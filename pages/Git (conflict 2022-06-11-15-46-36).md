- Relate
	- #Syncthing #版本管理 #团队协作 #软件工程 [[MyHulu/archive/MyLogseq/pages/github]] [[GitBook]]
- 01-成品文章
  collapsed:: true
	- 暂无
- 02-半成品卡片
	- 网站
		- [[MyHulu/archive/MyLogseq/pages/github]]
		- [[Gitlab]]
		- [[码云]]
	- 工具
		- [[TortoiseGit]]
		- [[sourcetree]]
		- [[vscode]]
		- [[网盘]]
	- git强制拉取并覆盖本地代码
		- ```
		  git fetch --all
		  git reset --hard origin/master
		  git pull
		  ```
		- git fetch --all
		- git reset --hard origin/master
		- git pull
	- git忽略文件夹除了xx文件
	  collapsed:: true
		- 比如有个文件夹，cache文件夹，我们要忽略除了cache文件夹的index.html文件，其他的文件都忽略掉，规则如下：
			- **/cache/*
			- !**/cache/index.html
	- 将一个本地文件夹配合同步网盘作为远程仓库
	  collapsed:: true
		- 直接在本地初始化remote仓库就可
			- git init --bare
		- 然后将可以将本地路径当做remote仓库路径了，可以代替github的ssh路径
	- 怎样生成SSH 公钥
	- 如何配置多个SSH，比如一个用于访问Github，一个用于访问Gitee
	  collapsed:: true
		- 虽然可以这么做，但不推荐，增加复杂度了，直接用一个公钥更好
	- git更新忽略文件
	  collapsed:: true
		- 更新了.gitignore配置文件后，需要更新整个缓存区
		- ```shell
		  git rm -r --cached .
		  git add .
		  git commit -m 'update .gitignore'
		  ```
	- 为计算机上的每个仓库设置 Git 用户名
	  collapsed:: true
		- 配置用户名
			- git config --global user.name "Mona Lisa"
		- 检查是否配置正确
			- git config --global user.name
	- Github Action
	  collapsed:: true
		- 1. [Github Action你值得了解的~ - 掘金](https://juejin.cn/post/6844904048794042382)
		- 2. [4个提高效率的GitHub Actions技巧-InfoQ](https://www.infoq.cn/article/ebfoucksujlm5aek8hoz)
		- 3. [GitHub Actions 入门教程 - 阮一峰的网络日志](https://www.ruanyifeng.com/blog/2019/09/getting-started-with-github-actions.html)
- 03-碎片笔记
  collapsed:: true
	- [[git备忘]]
	- [[git init 和 git init –bare 的区别]]
	- [[git备忘]]
	- [[git更新忽略文件]]
	- github
	- github镜像镜像网站
		- ![[Screenshot_2021-12-02-03-48-15-85.jpg]]
	- [[Github收藏]]
	- Gitlab
- 04-收集资料
	- 书籍
		- [Pro Git（中文版）](http://git.oschina.net/progit/index.html) 来自码云
		- [GitHub Docs](https://docs.github.com/cn/get-started/quickstart/hello-world) 来自Github
		- [Git权威指南 — GotGit](http://www.worldhello.net/gotgit/)
		- [Git - Book](http://git-scm.com/book/zh/v2) 来自git-scm.com
		- [連猴子都能懂的Git入門指南 | 貝格樂（Backlog）](https://backlog.com/git-tutorial/tw/)
	- 文章
		- [轮子那点事儿(2)：获取GitHub Followers, Stars, Forks的API的制作 | Lazy_V's Blog](http://blog.zhangkexuan.cn/2020/11/05/api-fanscount-github/)
		-
-
-