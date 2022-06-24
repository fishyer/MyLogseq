public:: true

- 来源
	- [配置 Logseq 自动发布相关流程](https://logseq.abosen.top/#/page/%E9%85%8D%E7%BD%AE%20logseq%20%E8%87%AA%E5%8A%A8%E5%8F%91%E5%B8%83%E7%9B%B8%E5%85%B3%E6%B5%81%E7%A8%8B)
		- 怕他删库，所以备份了一下，同时补充了一些注意点(高亮部分就是我补充的)
- 核心Action
	- [Logseq publish action](https://github.com/marketplace/actions/logseq-publish)
- ## 发布到其他仓库
	- 静态文件单独存储在了其他仓库，该仓库已经配置了发布到vercel的相关流程
	- `JamesIves/github-pages-deploy-action@v4` 可以配置目标 `repository-name`, 以发布到其他仓库。
	  默认的Action权限只限于当前仓库，要对其他仓库进行操作需要单独配置一个TOKEN。
- ## 修改 `index.html` 以注入自定义功能
	- 在本地维护脚本：`logseq/inject.html`
	  collapsed:: true
		- 这里主要是解决 [[Logseq 接入评论系统]] 中的相关问题
		- ==注意修改第11行，加入自己的giscus配置==
			- [GitHub Discussions 快速入门 - GitHub Docs](https://docs.github.com/cn/discussions/quickstart)
			- 开启giscus的三个条件
				- 1-此仓库是公开的，否则访客将无法查看 discussion。
				- 2-Discussions功能已在你的仓库中启用。
					- 在仓库的setting-General页面，往下翻，找到Discussions，按照引导开启并创建一个评论。
				- 3-giscus app 已安装否则访客将无法评论和回应。 [GitHub Apps - giscus](https://github.com/apps/giscus)
			- 在这个页面- [giscus](https://giscus.app/zh-CN)，可以生成需要粘贴的代码
				- 只需要填入仓库名和分类名即可，其它不要管，js代码会自动生成，复制即可
		- ``` html
		  			  <!-- 评论系统放置在主内容区域 -->
		  			  <script>
		  			      var container = document.getElementById('main-content-container');
		  			      container.style['flex-wrap'] = 'wrap';
		  			      container.firstChild.style['flex-basis'] = '100%';
		  			      var element = document.createElement('div');
		  			      element.classList.add('giscus');
		  			  	container.appendChild(element);
		  			  </script>
		  			  <!-- 评论系统 -->
		  			  <script src="https://giscus.app/client.js" ... async></script>
		  			  <!-- SPA 评论系统刷新问题 -->
		  			  <script>
		  			      history.pushState = (f => function pushState() {
		  			          var ret = f.apply(this, arguments);
		  			          window.dispatchEvent(new Event('pushstate'));
		  			          window.dispatchEvent(new Event('locationchange'));
		  			          return ret;
		  			      })(history.pushState);
		  			      history.replaceState = (f => function replaceState() {
		  			          var ret = f.apply(this, arguments);
		  			          window.dispatchEvent(new Event('replacestate'));
		  			          window.dispatchEvent(new Event('locationchange'));
		  			          return ret;
		  			      })(history.replaceState);
		  			      window.addEventListener('popstate', () => {
		  			          window.dispatchEvent(new Event('locationchange'))
		  			      });
		  			      window.addEventListener('locationchange', function() {
		  			          const iframe = document.querySelector('iframe.giscus-frame');
		  			          const title = decodeURIComponent(location.hash.split('/').slice(-1)[0]);
		  			          console.debug("location change to:", title, iframe);
		  			          if (!iframe || !title) return;
		  			          iframe.contentWindow.postMessage({
		  			              giscus: {
		  			                  setConfig: {
		  			                      term: title
		  			                  }
		  			              }
		  			          }, 'https://giscus.app');
		  			          console.debug("try refresh giscus:", title);
		  			      }, false);
		  			  </script>
		  			  <!-- 评论系统主题随logseq变化 -->
		  			  <script>
		  			      localStorage.setItem = (f => function setItem() {
		  			          var ret = f.apply(this, arguments);
		  			          if (arguments.length > 1 && arguments[0] == 'theme') {
		  			              window.dispatchEvent(new Event('themechange'));
		  			          }
		  			          return ret;
		  			      })(localStorage.setItem);
		  			  
		  			      window.addEventListener('themechange', () => {
		  			          const logseqTheme = JSON.parse(window.localStorage.getItem('theme'));
		  			          const lsq2gisThemeMap = {
		  			              'dark': 'dark_dimmed',
		  			              'white': 'light'
		  			          };
		  			          const giscusTheme = lsq2gisThemeMap[logseqTheme];
		  			          const iframe = document.querySelector('iframe.giscus-frame');
		  			          if (iframe && giscusTheme) {
		  			              iframe.contentWindow.postMessage({
		  			                  giscus: {
		  			                      setConfig: {
		  			                          theme: giscusTheme
		  			                      }
		  			                  }
		  			              }, 'https://giscus.app');
		  			              console.debug("try switch giscus theme:", giscusTheme);
		  			          }
		  			      });
		  			  </script>
		  ```
	- 在 CI 中修改 `index.html` 文件
		- ``` yaml
		  			  steps:
		  			     - name: Inject Script
		  			       run: sed -i "s@</body>@$( cat logseq/inject.html | tr '\n' ' ' | sed 's@&@\\&@g' )</body>@"  www/index.html
		  ```
			- 读取注入文件 → 整合为一行 → 对`&`进行转义 → 插入到`</body>`标签前
		- Relate Notes
			-
			-
- Github workflow
	- ``` yml
	  		  # This is a basic workflow to help you get started with Actions
	  		  
	  		  name: CI
	  		  
	  		  # Controls when the workflow will run
	  		  on:
	  		    push:
	  		      branches: [main]
	  		  
	  		    # Allows you to run this workflow manually from the Actions tab
	  		    workflow_dispatch:
	  		  
	  		  # A workflow run is made up of one or more jobs that can run sequentially or in parallel
	  		  jobs:
	  		    # This workflow contains a single job called "build"
	  		    build:
	  		      # The type of runner that the job will run on
	  		      runs-on: ubuntu-latest
	  		  
	  		      # Steps represent a sequence of tasks that will be executed as part of the job
	  		      steps:
	  		        # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
	  		        - uses: actions/checkout@v2
	  		        - name: change config.edn and custom.css
	  		          run: cp logseq/config-public.edn logseq/config.edn
	  		        - name: Logseq Publish 🚩
	  		          uses: pengx17/logseq-publish@main
	  		        # Inject custom scripts
	  		        - name: Inject Script
	  		          run: sed -i "s@</body>@$( cat logseq/inject.html | tr '\n' ' ' | sed 's@&@\\&@g' )</body>@"  www/index.html
	  		        # to make sure asset paths are correctly identified
	  		        - name: add a nojekyll file
	  		          run: touch $GITHUB_WORKSPACE/www/.nojekyll
	  		        - name: Deploy 🚀
	  		          uses: JamesIves/github-pages-deploy-action@v4
	  		          with:
	  		            repository-name: qbosen/qbosen.github.io
	  		            branch: main # The branch the action should deploy to.
	  		            folder: www # The folder the action should deploy.
	  		            clean: true
	  		            single-commit: true
	  		            token: ${{ secrets.TOKEN }}
	  ```