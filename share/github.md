- Github-Action
- [Actions](https://github.com/fishyer/MyLogseq/actions)
- 部署流程
	-
- Github Action数量限制
	- [Billing](https://github.com/settings/billing)
	- [管理 GitHub Actions 的支出限额 - GitHub Docs](https://docs.github.com/cn/billing/managing-billing-for-github-actions/managing-your-spending-limit-for-github-actions)
	- 每个月免费2000分钟的时长,每天平均66分钟
	- 每次部署大概需要3分钟，每天平均22次
	- 最好设置auto commit的周期为半个小时一次
- 常见问题
	- 1-Error: The deploy step encountered an error: The process '/usr/bin/git' failed with exit code 128
		- Go to repo settings
		- Select Actions -> General
		- In Workflow permissions, select Read and write permissions
		- ![](https://image.fishyer.com/202205082326837.png)
- 收集资料

- 星标
  collapsed:: true
	-
- 集锦
  collapsed:: true
	- Analysis-源码解析系列
	- Practice-项目实战系列
	- Refactor-设计重构系列
- github pages地址
  collapsed:: true
	- git@github.com:fishyer/fishyer.github.io.git\
- Github授权登录，明明已经新建用户成功了，但是无法跳转回去，一直停留在授权之后的页面
  collapsed:: true
	- You are being redirected to the authorized application.
	- If your browser does not redirect you back, please click here to continue.
	- http://localhost:3000/api/oauth/redirect?code=261a412d777835f2a720
	- 可能是回调地址不正确。
-
-
-
-