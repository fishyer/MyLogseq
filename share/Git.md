- Relate
	- #Syncthing #版本管理 #团队协作 #软件工程 [[MyHulu/archive/MyLogseq/pages/github]] [[GitBook]]
- 01-成品文章
  collapsed:: true
	- 暂无
- 02-半成品卡片
	- 网站
		- [[MyHulu/archive/MyLogseq/pages/github]]
		- [[MyObsidianNote/Inbox/Gitlab]]
		- [[码云]]
	- 工具
		- [[TortoiseGit]]
		- [[MyObsidianNote/Inbox/sourcetree]]
		- [[MyObsidianNote/Archive/01-Inbox/vscode]]
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
	- git设置代理
		- git config --global http.proxy http[s]://fishyer:fishyer182047@127.0.0.1:8888
	-
- 03-碎片笔记
  collapsed:: true
	- [[MyObsidianNote/Archive/01-Inbox/git备忘]]
	- [[MyObsidianNote/Archive/01-Inbox/git init 和 git init –bare 的区别]]
	- [[MyObsidianNote/Archive/01-Inbox/git备忘]]
	- [[git更新忽略文件]]
	- github
	- github镜像镜像网站
		- ![[Screenshot_2021-12-02-03-48-15-85.jpg]]
	- [[MyObsidianNote/Archive/01-Inbox/Github收藏]]
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
- 生成本机的SSH
	- ssh-keygen -t rsa -C "your_email@example.com"
- git checkout master 报错 error: invalid path ‘文件路径’
	- git config core.protectNTFS false
	- 查了下官方手册，官方原话： If set to true, do not allow checkout of paths that would cause problems with the NTFS filesystem
	- 大概意思是说NTFS有个路径保护机制，防止文件系统出错。
		- [git checkout master 报错 error: invalid path ‘文件路径‘_城南199的博客-CSDN博客](https://blog.csdn.net/qq_38209921/article/details/115716421)
- 更新git忽略文件
	- git rm -r --cached .
	- git add .
	- git commit -m "update .gitignore"
- 常见问题
  collapsed:: true
	- 提交commit以后自动push
		- 添加
			- .git/hooks/post-commit
			  "#!/bin/sh
			  
			  git push origin main"
			-
	-
- Git Hooks 
  collapsed:: true
	-
- Github-Action
  collapsed:: true
	- [Actions](https://github.com/fishyer/MyLogseq/actions)
	- 部署流程
		-
	- Github Action数量限制
		- [Billing](https://github.com/settings/billing)
		- [管理 GitHub Actions 的支出限额 - GitHub Docs](https://docs.github.com/cn/billing/managing-billing-for-github-actions/managing-your-spending-limit-for-github-actions)
		- 每个月免费2000分钟的时长,每天平均66分钟
		- 每次部署大概需要3分钟，每天平均22次
		- 最好设置auto commit的周期为半个小时一次
			- 先测试10分钟一次试试
	- 常见问题
		- 1-Error: The deploy step encountered an error: The process '/usr/bin/git' failed with exit code 128
			- Go to repo settings
			- Select Actions -> General
			- In Workflow permissions, select Read and write permissions
			- ![](https://image.fishyer.com/202205082326837.png)
- git全局配置
	- git config --global http.proxy http[s]://userName:password@proxyaddress:port
	- git config --global http.proxy http[s]://userName:password@proxyaddress:port
	- git config --global http.proxy http[s]://fishyer:fishyer182047@127.0.0.1:10809
-
-