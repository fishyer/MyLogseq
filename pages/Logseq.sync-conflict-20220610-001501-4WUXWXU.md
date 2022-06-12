public:: true

- 01-成品文章
  collapsed:: true
	- 暂无
- 02-半成品卡片
	- 用Logseg帮助我们实现从==碎片化==到==体系化==
	  collapsed:: true
		- 其实就是添加标签，不过这个标签比起传统标签，在于它本身也是一个页面，可以添加备注，用于沉淀和聚合相关信息。
		- 概述
			- 各种碎片信息-->标签-->根目录树，通过这套流程将散乱的碎片信息，和我们的体系化的根目录树联系起来，借助标签的反向链接来实现信息的聚合汇总。
			- 我这里说的标签，其实就是双链，因为在Logseq里面两者其实是一致的
			- 将常用标签的双链，放到右侧常驻的根目录里面，没有放在根目录里面的笔记，很快就会被淹没的
			- 我现在在logseq，就是用contents.md这个文件来做根目录的
		- 流程
			- 关于标签、反向链接、根目录树的一个体系化整理流程
			- 1. 在日常的收集中，记得给一些比较重要的笔记添加标签
				- 比如我现在在刷胶泥老师的ob课程，就在这个课程笔记中，添加#ReadLater标签
					- ![](https://image.fishyer.com/202205090550051.png)
				- 还有同时在刷L先生说的公众号合集，也在这里打个#ReadLater标签
					- ![](https://image.fishyer.com/202205090551483.png)
			- 2. 在根目录中设置此标签的双链的合适位置，以便我们可以根目录下随时查看它，也可以在此处双链引用的子列表中添加需要重点关注的内容和临时记录(建议临时记录折叠一下)
				-
			- 3.点击根标签树中的标签引用，就可以看到所有本标签的汇总信息了
				- 所谓根标签树，就是自己维护一个重点关注的标签大纲(不超过10个)，并设置好层级关系(不超过2级)
				- ![](https://image.fishyer.com/202205090552086.png)
	- Logseq可以用来干嘛？
	  collapsed:: true
		- 用来记日记，记录每天的各种零散想法
		- 用来当做大纲来辅助思考，让思维不再混乱无序
		- 用来当做MarkDown编辑器来写作，所见即所得
		- 用来搭建个人wiki知识库，并用双链的潜在链接来自动聚合，防止笔记坟场
	- 为什么推荐Logseq做笔记？
	  collapsed:: true
		- 1-它有大纲、MarkDown、双链等功能，还是本地的，免费的，开源的，编辑体验也超爽
		- 2-它的自动聚合功能超爽，可以帮我们发现笔记之间的潜在链接，让以前的笔记不至于石沉大海
			- 案例效果，来源于[双链笔记软件推荐：Logseq 和它的五种用法 - 少数派](https://sspai.com/post/69503)
			  collapsed:: true
				- ![](https://photo.fishyer.com/img/202204212126602.png)
	- 给Logseq新手的建议
	  collapsed:: true
		- 1-就当一个普通的[[大纲]]软件来用就行了，Tab键变成下级节点，Shift+Tab变成上级节点
		- 2-就当一个普通的[[MarkDown]]软件就行了，## 二级标题，### 三级标题，更多语法看[这里](https://cubox.pro/share/bWpE42)
		- 3-就当一个普通的[[双链]]笔记软件来用 就行了，`[[]]`就是另一条笔记联系起来，可以当标签来用
		- 4-多用`/`命令，里面有很多快捷输入的方法，不用自己记语法
		- 不建议新手去玩的功能
		  collapsed:: true
			- 别名
				- 比如给一个页面取多个标题，方便在不同地方引用它
					- ```
					  alias:: title1 title2
					  ```
			- 嵌入
				- 比如嵌入一个页面
					- ```
					  {{embed [[SubPage]]}}
					  ```
			- 高级Query
				- 不过简单的Query语法可以了解一下，
					- 查找所有属性为public，值为false的笔记
						- ```
						  {{query (property public false)}}
						  ```
	- 不建议用Logseq去做的事
	  collapsed:: true
		- 个人使用Logseq的一些心得
		- 不建议用Logseq做PDF阅读，推荐[[Zotero]]，因为Logseq不方便管理书架
		- 不建议用Logseg做任务管理，推荐[[滴答清单]]，因为滴答清单收集任务和日程提醒更方便
		- 不建议用Logseq做文章分享，推荐[[MWeb]] 或 [[MyHulu/archive/MyLogseq/pages/Notion]]，因为大纲很适合自己整理思路，保持简洁，但不是这种特殊的MarkDown形式不是特别便于分享，并且它也没有直接发布到各种自媒体平台的插件
			- 当然，如果你想以双链笔记的形式分享，那Logseq是不二之选
	- Obsidian与Logseq的对比
	  collapsed:: true
		- Obsidian的劣势
		  collapsed:: true
			- 1.Obsidan更偏向Markdown，对于大纲的支持不是特别好，适合写长文，但不是很适合整理思路
			- 2.Obsidian的所见即所得，没有Logseq用起来爽
			- 3.Obsidian的潜在链接不是很方便查看时编辑，无法直接在当前page编辑它的潜在链接的那个block，点击潜在链接的block，会自动跳转到那个block所在的page，有点麻烦
			- 4.Obsidian没有Logseq的导出html功能，不方便用来建站
			- 5.Obsidian的块引用没有Logseq方便，是基于##标题的
		- Obsidian的优势
		  collapsed:: true
			- 1.Obsidian的插件更加丰富
			- 2.Obsidian的流畅度更好一点，毕竟它不算严格的块编辑器，节点主要是page级别，底层的数据库的压力不是特别大，这点在移动端时会比较明显
			- 3.Obsidian的潜在链接比较方便快速关联，目前Logseq还没有这方面的快捷方式，可能需要借助PopClip
			- 4.Obsidian可直接查看文件夹体系，管理附件会比较方便
			- 5.如果舍得花钱的话，Obsidan官方有同步和发布功能，Logseq暂时还没有
	- 我自己整理的在日常使用Logseq的过程中遇到的一些问题
	  collapsed:: true
		- DONE 目前Logseq还没有一键收藏别人分享的Logseq页面功能，复制粘贴时，会发现只能复制一个节点
			- 好在可以借助Cubox的收藏，实现网页快照保存，以免别人的博客挂了导致链接失效
		- TODO 准备发布文章时，如何将Logseq的大纲形式转换为标准MarkDown形式？
		  collapsed:: true
			- 自己刚准备用sed来做下批量替换时，突然发现网上已经有大神写好了脚本
			  collapsed:: true
				- [logseq转换为标准markdown脚本](https://xutuan.vercel.app/#/page/logseq%E8%BD%AC%E6%8D%A2%E4%B8%BA%E6%A0%87%E5%87%86markdown%E8%84%9A%E6%9C%AC)
			- 脚本
			  collapsed:: true
				- ```
				  # convert logseq to md
				  for file in *.md **/*.md **/**/*.md 
				  do
				  	# filepath="$file"
				  	file_name=$(basename "$file")
				  	echo "PROCESSING $file..."
				  	queryb='#+BEGIN_QUERY'
				  	querye='#+END_QUERY'
				  	sed -i 's/##########/\t\t\t\t\t\t\t-/' $file
				  	sed -i 's/#########/\t\t\t\t\t\t-/' $file
				  	sed -i 's/########/\t\t\t\t\t-/' $file
				  	sed -i 's/#######/\t\t\t\t-/' $file
				  	sed -i 's/######/\t\t\t-/' $file
				  	sed -i 's/#####/\t\t-/' $file
				  	sed -i 's/####/\t-/' $file
				  	sed -i 's/###/-/' $file
				  	# sed -i 's/##//' $file
				  	sed -i 's/:PROPERTIES:/<!--/' $file
				  	sed -i 's/:END:/-->\n/' $file
				  	sed -i 's/{{{embed /#relink-embed <!--/' $file
				  	sed -i 's/((/#relink-block [[/' $file
				  	sed -i 's/))/]]/' $file
				  	sed -i 's/{{{/#relink <!--/' $file
				  	sed -i 's/}}}/-->/' $file
				  	sed -i 's/{{/#relink <!--/' $file
				  	sed -i 's/}}/-->/' $file
				  	sed -i "s/$queryb/<!--$queryb/" $file
				  	sed -i "s/$querye/$query-->\n\n/" $file
				  done
				  ```
			- 步骤
			  collapsed:: true
				- 代码保存为`convertlogseq.sh`
				- 将需要转换的markdown文件与脚本放在同一个文件夹下
				- cmd-cd进入待处理的文件夹路径
				- 运行 > `convertlogseq.sh`
			- 哈哈，感觉配合MWeb的发布前脚本配置，完美
		- DONE 如何发布Logseq为博客？
		  collapsed:: true
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:20:56]--[2022-04-23 Sat 18:20:56] =>  00:00:00
		  :END:
			- DONE 1-本地导出为html，上传到github，借助vercal的部署服务，借助CloudFlare做重定向
			  :LOGBOOK:
			  CLOCK: [2022-04-23 Sat 18:44:26]--[2022-04-23 Sat 18:44:27] =>  00:00:01
			  :END:
		- TODO logseq没有像WorkFlowy那样的@标签，感觉制作一些人名标签时不是很方便
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:44:15]--[2022-04-23 Sat 18:44:16] =>  00:00:01
		  :END:
		- TODO logseq的block有方便的移动方式么？
		- TODO logseq的图片自动上传插件 ImageUploader好像在0.6.6以后又不行了
		- TODO logseq的默认日志文件名称，修改了配置文件，但好像只能修改显示效果，不会修改实际文件名
		- WAITING 一次导入太多Markdown文件到Logseq库里面，导致卡顿怎么办
			- 无解，不过现在好像优化了很多，现在好像不怎么卡了
		- TODO logseq导入的zotero标注，都找不到anotations，只有一些元数据
		- DONE 如何获取笔记的URL Schema，以方便和其它工具联动
		  collapsed:: true
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:06:08]--[2022-04-23 Sat 18:06:09] =>  00:00:01
		  :END:
			- 右上角，Copy page URL
			- ```
			  logseq://graph/MyLogseq?page=Contents
			  ```
		- DOING 在外部点击logseq的url，会新建一个窗口，而不是复用原来的窗口，据说已有PR，但尚未正式发布
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:07:23]
		  :END:
		- DONE 如何定制首页
		  collapsed:: true
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:07:30]--[2022-04-23 Sat 18:07:30] =>  00:00:00
		  :END:
			- 比如你想让你的overview页面作为博客首页,还是打开config.edn这个文件, 然后输入如下内容
				- ```
				  :default-home {:page "overview":sidebar "Contents" }
				  ```
		- DONE 如何自定义主题
		  collapsed:: true
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:19:37]--[2022-04-23 Sat 18:19:38] =>  00:00:01
		  :END:
			- 修改logseq/config.edn，即可
			- 可以配置Github仓库里面的的远程文件做主题，[Logseq主题](https://gist.github.com/3e82a313a58b816a7ddf6de25a607977)
				- 使用[[jsdelivr]]给github文件做cdn加速
		- DONE 如何添加页面别名，方便在不同的引用地方使用不同的名称
		  collapsed:: true
		  :LOGBOOK:
		  CLOCK: [2022-04-23 Sat 18:17:47]--[2022-04-23 Sat 18:17:48] =>  00:00:01
		  :END:
			- [term/alias](https://docs.logseq.com/#/page/term%2Falias )
			- ```
			  alias:: title1 title2
			  ```
	- 网上的公开Logseq数字花园案例
	  collapsed:: true
		- [fishyer.com](https://fishyer.com)
		- [abosen-README](https://logseq.abosen.top/#/page/README)
		- [xutuan-logseq使用经验分享](https://xutuan.vercel.app/#/page/logseq%E4%BD%BF%E7%94%A8%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB)
		- [zhangxueshan246-Logseq](https://zhangxueshan246.github.io/#/)
		- [tothegarden-All journals](https://tothegarden.vercel.app/all-journals)
- 03-碎片笔记
  collapsed:: true
	- Logseq笔记
	- lodseq导出
	  collapsed:: true
		- ![](MyAttachment/Screenshot_2021-12-02-06-03-35-85.jpg)
	- Logseq
	  collapsed:: true
		- public:: true
		- [官方帮助文档](https://logseq.github.io/#/page/getting%20started)
		- 我的公开Logseq文章仓库
			- 启动页
		- 概述
			- collapsed:: true
			- 本地优先，你的数据不会上传服务器，可以完全离线使用
			- 没有 lock-in，使用 markdown/org-mode 格式来存储数据，可以轻松地跟其他软件协作
			- 可玩性，项目是开源的，大家可以愉快地 hack，之后马上也会有插件系统 & API
			- 有 web 版本和本地 app 可下载
		- 主要功能
			- collapsed:: true
			- 大纲笔记，高频，每天N次，速记和整理用
			- 双向链接，高频，和标签和目录树配合，汇总信息很方便
			- GTD状态，高频，每天安排任务，跟踪执行耗时，很方便
			- MarkDown，中频，大概每周一次，写文章用
			- PDF阅读标注，中频，大概每周一次吧，主要是学习PDF书籍用
			- 闪卡，低频，暂时没用
		- 使用杂谈
			- collapsed:: true
			- [[Logseq-从碎片化到体系化]]
			- [[Logseq和Obsidian的配合与对比]]
			- 用右侧的目录来代替左侧的收藏页面，因为目录可以展开、编辑、拖动，而收藏只能点击
			- 把Logseq文件夹用[[syncthing]]和[[Git]]管理起来，前者解决垃圾箱和多设备同步，后者解决版本管理
			- 感觉Logseq真的非常方便研究性学习，在研究一个东西时，过程中遇到的一切问题，搜集到的一切资料，自己的一切想法，都可以很方便的记录在这里
		- 特色亮点 #good
			- collapsed:: true
			- 做==PDF阅读和标注==非常棒，可以高亮文字和截图，点击可跳转回原始页码
				- 只是贴的高亮文字，在笔记里面显示的页码太抢眼了，希望可以隐藏掉或自定义样式
			- 完美融合了==大纲和Markdown==，虽然它的Markdown在别的软件打开不是非常完美，但在Logseq里面显示效果真的很好
				- collapsed:: true
				- 其实Markdown可以当做json一样，是笔记工具之间的数据交换格式，但是显示时，完全可以有自己的自定义显示效果，就算Logseq创建的md在Obsidian显示效果不是完美，但也能用了
		- 存在问题 #bad
			- collapsed:: true
			- 不是很方便将一个==块快速转换为页面==，就像Notion那样，现在只能剪切粘贴，略显麻烦
			- 分享的网页中，==简书图床不能显示==，阿里云图床可以显示，本地图片可以显示
				- 使用Obsidian的local images插件下载简书图床的图片到本地 #Obsidian插件
				- 然后正则替换一下格式
					- MyLogseq/assets
					- ../assets
			- ==选中文字后添加外链==，不是很方便，不能像内联那样按两下`[`就好了
			- 性能问题
				- Logseq在开发数据库版本了，以后文件增长带来的性能需求不会是问题
			- page和block转换的问题
				- -
		- 怎么做任务管理-journals
			- collapsed:: true
			- Logseq做时间管理
				- 思维导图
					- collapsed:: true
					- ![image.png](image_1638513388051_0.png)
				- 任务状态-5种状态
					- -NOW 当前正在关注或执行的，相当于工作台
						- :LOGBOOK:
							- CLOCK: [2021-12-03 Fri 14:37:49]
							- CLOCK: [2021-12-03 Fri 14:37:51]
							- CLOCK: [2021-12-03 Fri 14:37:53]
							- CLOCK: [2021-12-03 Fri 14:37:58]
							- CLOCK: [2021-12-03 Fri 14:38:04]
							- :END:
					- -LATER 稍后准备做的，相当于下一步行动
					- -DONE 已完成的任务
					- -WAITING 等待时机，将来也许要做，远期目标
					- -CANCELLED 暂时搁置的任务，备忘录
				- 任务优先级 /ABC
					- DONE [#A] 任务1
						- :LOGBOOK:
							- CLOCK: [2021-12-03 Fri 14:48:37]--[2021-12-08 Wed 10:14:41] =>  115:26:04
							- :END:
					- DONE [#B] 任务2
						- :LOGBOOK:
							- CLOCK: [2021-12-03 Fri 14:48:56]--[2021-12-08 Wed 10:15:25] =>  115:26:29
							- :END:
					- DONE [#C] 任务3
						- :LOGBOOK:
							- CLOCK: [2021-12-03 Fri 14:49:14]--[2021-12-08 Wed 10:15:29] =>  115:26:15
							- :END:
				- 任务的日程表
					- collapsed:: true
					- DONE 任务11
						- SCHEDULED: <2021-12-05 Sun>
							- :LOGBOOK:
							- CLOCK: [2021-12-03 Fri 15:00:44]
							- CLOCK: [2021-12-03 Fri 15:00:57]
							- :END:
					- 参考
						- [OKR + GTD + Note => Logseq - 知乎](https://zhuanlan.zhihu.com/p/369386414) #OKR
							- OKR的5个重要概念
								- ![image.png](image_1638515209528_0.png)
							- [找到最重要的事](https://mp.weixin.qq.com/s/1T8r7HIX8NAQqUowFOV0rg)
								- ![image.png](image_1638515495287_0.png)
							- 4个个人愿景
								- 身体提升：拥有一个健康的身体；
								- 能力提升：提升技术到价值的转化效率；
								- 收入提升：家庭财务状况健康；
								- 影响力提升：在技术和投资领域建立专业影响力。
							- Dawei Ma的OKR案例
								- 2021-OKR-O1-KRs
									- 每月熬夜不超过4次
									- 减肥5斤
								- 2021-OKR-O2-KRs
									- 打造一个流量站，月PV达 100K
				- 打造一个英文内容权威站，月PV达 10K，月盈利达 $500
				- 参加五次头马活动并至少演讲一次，发表3篇英文文章
				- 2021-OKR-O3-KRs
					- 被动收入投资组合年复合收益率超 15%
				- 2021-OKR-O4-KRs
					- 在博客技术与投资领域分别输出超过10篇文章
				- 由KR来聚拢TASK
					- ![image.png](image_1638516246874_0.png)
				- -
			- Now
			- Later
		- 怎么做笔记管理-pages
		- 怎么做附件管理-assets
			- collapsed:: true
			- Logseq做文件管理
				- collapsed:: true
				- 直接拖动
				- /Users/yutianran/Documents/待处理md/使用Teambition进行团队任务管理.md
				- file:///Users/yutianran/Documents/%E5%BE%85%E5%A4%84%E7%90%86md/%E4%BD%BF%E7%94%A8Teambition%E8%BF%9B%E8%A1%8C%E5%9B%A2%E9%98%9F%E4%BB%BB%E5%8A%A1%E7%AE%A1%E7%90%86.md
				- -
		- 怎么分享自己写的Logseq笔记
			- collapsed:: true
			- Logseq发布
				- Logseq发布流程
					- -
						- 1. 标记页面为public:: true
					- -
						- 2. 导出图谱-Export public pages，选择路径为MyPKM-Publish
					- -
						- 3. 打开SourceTree，提交+推送到Github Pages仓库，它的上传有点慢，可能需要2-3分钟，稍等一下就好
				- 遇到问题
					- -
						- 1. 上传到github.io的速度有点慢，不知道是不是自己网络问题
					- -
						- 2. 本地可以查看图床，发布出去的网页却没法查看图床了，奇怪
						- 不是所有外链图片都不显示，只有简书的才不显示，阿里云可以显示
						- 有没有可以自动下载Markdown的网络图片并替换为本地图片的插件？
							- pic-migrater [利用PicGo快速迁移Weibo外链图片到GitHub - Pockies | 博客](https://pockies.github.io/2019/04/27/weibo-to-github/)
							- 其实自己写一个python脚本来处理也可以 [利用PicGo快速迁移Weibo外链图片到GitHub - Pockies | 博客](https://pockies.github.io/2019/04/27/weibo-to-github/) #TODO
					- 3.
			- -
		- 怎么和其它软件联动
			- collapsed:: true
			- #VSCode 脚本处理
			- #Finder 系统文件管理
			- #Obsidian md各种复杂的管理
			- #Typora md所见即所得编辑
			- #Zotero 文献管理
			- #Syncthing 多设备同步
			- #git 版本管理
			- #WorkFlowy 大纲编辑
			- #pCloud 增量备份网盘
			- #飞书 速记，随时添加想法
			- #滴答清单 任务管理，随时添加任务
		- 自带的特色功能
		- 案例收藏
			- Logseq的三种使用场景
				- -
		- 重要资料
			- [Logseq-官网](https://logseq.com/)
			- [Logseq-中文社区](https://cn.logseq.com/categories)
			- [Logseq-Github下载地址](https://github.com/logseq/logseq/releases)
			- [Logseq 系列教程-FinnYan](https://www.finncode.cn/logseq/#/page/1.1%20%E5%85%B3%E4%BA%8E%20Logseq)
			- HomePage: https://logseq.com/
				- Github: https://github.com/logseq/logseq
					- 英文 Discord: https://discord.com/invite/KpN4eHY
					- 中文 Discord: https://discord.com/invite/SVmDc9xvQV
					- Roadmap: https://trello.com/b/8txSM12G/logseq-roadmap
					- 论坛： https://discuss.logseq.com/ & https://cn.logseq.com/
			- [分享:使用logseq + gitee发布的页面，内含教程 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1396)
			- [使用 logseq 部署个人页面](https://dale502.gitee.io/logseq-learn/#/page/%E4%BD%BF%E7%94%A8%20logseq%20%E9%83%A8%E7%BD%B2%E4%B8%AA%E4%BA%BA%E9%A1%B5%E9%9D%A2)
			- [logseq-learn-Contents](https://dale502.gitee.io/logseq-learn/#/page/contents)
		- 其它收藏
			- [logseq/logseq-plugin-samples: Logseq plugin samples for beginner 🌱](https://github.com/logseq/logseq-plugin-samples)
			- [App+1 | 卡片笔记纷至沓来，Logseq 凭何在我眼中独树一帜？ - 少数派](https://sspai.com/post/68459)
			- [logseq/logseq: A privacy-first, open-source platform for knowledge management and collaboration. Desktop app download link: https://github.com/logseq/logseq/releases, roadmap: https://trello.com/b/8txSM12G/roadmap](https://github.com/logseq/logseq)
		- Logseq的标签和双链很像啊，都会自动生成一个标签的页面
		- logseq快捷键
			- dsfa
			- DONE 快速搜索/新建笔记 cmd+K
				- :LOGBOOK:
					- CLOCK: [2021-12-02 Thu 20:30:47]--[2021-12-02 Thu 20:30:49] =>  00:00:02
					- CLOCK: [2021-12-02 Thu 20:31:00]--[2021-12-02 Thu 20:31:40] =>  00:00:40
					- :END:
		- logseq的大纲配合obsidian的 [[MarkDown]] ，简直就是完美配合
		- -
	- logseq-插件
	  collapsed:: true
		- ![](Screenshot_2021-12-02-06-02-40-89.jpg)
	- logseq-卡片大法
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-53-30-00.jpg)
		- ![](Screenshot_2021-12-02-05-54-46-61.jpg)
	- logseq-图谱、插件、导出
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-58-22-87.jpg)
		- logseq-zotero
		- ![](Screenshot_2021-12-02-05-59-42-14.jpg)
		- ![](Screenshot_2021-12-02-06-00-03-70.jpg)
	- logseq-bookxnote
	  collapsed:: true
		- ![](Screenshot_2021-12-02-06-16-41-23.jpg)
	- logseq-moc
	  collapsed:: true
		- logseq-bookxnote
		- logseq与其它软件的联动
		- logseq发布
		- logseq-插件
		- logseq-图谱、插件、导出
		- logseq-卡片大法
		- logseq-page
		- logseq高级搜索
		- logseq做闪卡
		- logseq做pdf阅读
		- logseq做文件管理
		- logseq做任务管理
		- logseq块编辑的常用用法
		- logseq教程
		- logseq快捷键设置
		- logseq中文社区
		- logseq实现闪卡
	- logseq-page
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-50-47-13.jpg)
	- logseq发布
	  collapsed:: true
		- ![](Screenshot_2021-12-02-06-06-49-06.jpg)
	- logseq高级搜索
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-42-31-89.jpg)
		- ![](Screenshot_2021-12-02-05-46-57-91.jpg)
		- ![](Screenshot_2021-12-02-05-48-24-83.jpg)
		- ![](Screenshot_2021-12-02-05-49-40-26.jpg)
	- Logseq和Obsidian的反向链接的显示对比与使用场景-汇总工作日报
	  collapsed:: true
		- #! https://zhuanlan.zhihu.com/p/441631584
		- # Logseq和Obsidian的反向链接的显示对比与使用场景-汇总工作日报
		- -
			- public:: true
		- #Logseq #Obsidian #双向链接
		- 缘起
			- 以前总觉得反向链接没啥用，最近看[双链笔记软件推荐：Logseq 和它的五种用法 - 少数派](https://sspai.com/post/69503)，get到了一种反向链接的用法
				- 可以用反向链接来做主题聚合，比如汇总工作日报
					- ![image.png](image_1638732451312_0.png)
		- 具体流程
			- 1.首先我们先在每日日志里面添加`[[工作日报]]`的内链
			- 2.然后就可以在Logseq和Obsidian查看了
				- Logseq的显示效果，一目了然，仿佛就在内容里，而且里面的大纲是可以折叠展开的
					- ![image.png](image_1638732391539_0.png)
				- Obsidian的显示效果，和内容是不同面板，不是很方便查看到引用了`[[工作日报]]`的具体内容
					- ![image.png](image_1638732426556_0.png)
		- 总结
			- 希望这个玩法能帮大家更好的理解双向链接，更好的用双向链接来帮自己做主题聚合
			- 另外，也强烈建议大家将Logseq和Obsidian搭配起来使用，不是说用Obsidian就不能用Logseq了
	- Logseq和Obsidian的配合与对比
	  collapsed:: true
		- public:: true
		- 缘起
			- 看到网上很多人在讨论Obsidian和Logseq这两个笔记软件哪个更好用，各有一群拥趸。喜欢用大纲做轻量记录和灵活整理的，偏向于Logseq。喜欢用MarkDown做图文混排的，偏向于Obsidian。
			- 不可否认，这两款工具都是非常棒的双链笔记工具，而且都支持本地存储，都是免费的。
			- 我最先接触的是Obsidian，一直把它当做自己的本地md文件管理器，用它对本地md文件进行全文搜索。但是感觉Obsidian还是更适合写文章，记录灵感的话，确实不是特别方便
			- 的MarkDown形式的记录方式，对于一些临时想法的记录而言，有点太笨重了，
			- 后来看到有网友说可以两者共用一个文件库。
			- 于是我去体验了一下
			- 是的，我现在就是Logseq和Obsidan共用一个文件库，名字就叫LogOb，几周的体验下来，感觉两者的亮点可以形成很好的配合，
		- 我的使用场景
			- -
				- 1. 用Logseq适合每天随时打开记录点什么，我一般都是让它固定在一屏的
			- -
				- 2. 至于Obsidian，一般是准备写文章的时候才用到，可能一周都才打开一次。
		- Logseq的亮点是：
			- -
				- 1. 主要编辑方式为大纲，非常适合碎片式记录，后续看能不能和Alfred配合一下
			- -
				- 2. PDF标注的体验很棒，高亮和截图都支持，看扫描版的PDF很爽
			- -
				- 3. 网页标注，配合Diigo的copy all，粘贴到这里，再调整一下层级关系，加一点自己的描述，就是不错的网页笔记了，还自带Diigo的网页备份链接
			- -
				- 4. 它的入链的展示方式，默认就在笔记的下方，就好像和笔记合为一体一样，比起Obsidian的单独面板展示，会更加自然一点，非常适合查看主题聚合
		- Obsidian的亮点：
			- -
				- 1. 主要编辑方式为Markdown，非常适合写长文章，Logseq也能写md，但是可能会自动添加- 等符号，还有一些Logseq的独有格式信息，可能会对md文档形成污染，不利于md文档发布到知乎等平台
			- -
				- 2. 插件非常丰富，会有许许多多的奇怪用法，比如Calendar插件的月度日历的展示形式，配合Logseq本身的时间线展示形式，就是一个很好的配合
			- -
				- 3. 目前Logseq还没有手机端，可以借助Obsidian的手机端来搜索查看Logseq的笔记
		- 总结
			- 两者都会有很多元数据，不仅仅只是笔记库，也可以当做结构化的数据库，很适合做一些高阶的查询、过滤、分组、展示等。
	- logseq汇总工作日报
	- logseq教程
	  collapsed:: true
		- ![](Screenshot_2021-12-02-04-30-13-09.jpg)
		- [Logseq小白系列教程入门篇一 - 知乎](https://zhuanlan.zhihu.com/p/343854552)
		- ![](Screenshot_2021-12-02-04-31-05-36.jpg)
		- ![](Screenshot_2021-12-02-04-31-42-78.jpg)
	- Logseq卡顿问题
	  collapsed:: true
		- Logseq的卡顿真的是太糟心了
		- 感觉每天在重建索引的时间都花了几个小时了
		- Logseq是怎么识别块的呢？
		- 大概有两千多个块吧
	- logseq块编辑的常用用法
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-28-45-63.jpg)
	- logseq快捷键设置
	  collapsed:: true
		- ![](Screenshot_2021-12-02-04-28-14-27.jpg)
		- gvim风格
	- logseq实现闪卡
	  collapsed:: true
		- ![](Screenshot_2021-12-02-03-28-04-93 1.jpg)
		- ![](Screenshot_2021-12-02-03-28-39-98.jpg)
		-
	- logseq使用模板
	  collapsed:: true
		- #Logseq
		- 创建模板
			- python代码模板
				- template:: python
			- ```python
				- print("hello python")
					- ```
		- -
		- 使用模板
			- `/TEM`
			- 选择指定模板即可
			- python代码模板
				- ```python
					- print("hello python")
						- ```
	- logseq与其它软件的联动
	  collapsed:: true
		- ![](Screenshot_2021-12-02-06-08-05-41.jpg)
	- logseq中文社区
	  collapsed:: true
		- ![](Screenshot_2021-12-02-03-50-48-29.jpg)
	- logseq做任务管理
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-33-48-61.jpg)
		- ![](Screenshot_2021-12-02-05-35-20-97.jpg)
	- logseq做闪卡
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-41-00-27.jpg)
		- ![](Screenshot_2021-12-02-05-41-29-57.jpg)
	- logseq做文件管理
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-36-15-67.jpg)
	- logseq做pdf阅读
	  collapsed:: true
		- ![](Screenshot_2021-12-02-05-37-55-98.jpg)
		- ![](Screenshot_2021-12-02-05-38-46-97.jpg)
	- Logseq-常用快捷键
	  collapsed:: true
		- 快速搜索或创建 cmd+O
		- 用默认软件打开
		- 添加收藏
		- 全选 cmd+shift+a
		- 切换任务状态 cmd+enter
		- Slash自动提示 /
		- 新建块 enter
		- 块中新建行 shift+enter
		- 当前页面搜索 cmd+shift+F
		- 侧边栏打开 cmd+shift+o
		- 最近记录上一页
		- 最近记录下一页
		- 插入链接
		- 在右侧边栏打开当日笔记，方便查看今日计划和记录今日已做
	- 我的公开Logseq文章仓库
	- 概述
	  collapsed:: true
		- 本地优先，你的数据不会上传服务器，可以完全离线使用
		- 没有 lock-in，使用 markdown/org-mode 格式来存储数据，可以轻松地跟其他软件协作
		- 可玩性，项目是开源的，大家可以愉快地 hack，之后马上也会有插件系统 & API
		- 有 web 版本和本地 app 可下载
	- 主要功能
	  collapsed:: true
		- 大纲笔记，高频，每天N次，速记和整理用
		- 双向链接，高频，和标签和目录树配合，汇总信息很方便
		- 任务状态，高频，每天安排任务，跟踪执行耗时，很方便
		- MarkDown，中频，大概每周一次，写文章用
		- PDF阅读标注，中频，大概每周一次吧，主要是学习PDF书籍用
		- 闪卡，低频，暂时没用
	- ==Logseq使用场景==
	  collapsed:: true
		- 任务管理-
			- 工作日报-
				- 学习大纲-慕课-极客时间
				- 读书笔记-微信读书和PDF
				- 每日日志-
				- 编程图谱-
				- 工具图谱-
				- 理财图谱-
				- 随笔文章-
		- Logseq适合速记一些块，以及阅读查看
		- 学习Logseq的时间管理和文件管理
			- 参考资料
				- [Logseq从入门到精通_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1144y14764?p=8)
				- [观雨放羊 - 知乎](https://www.zhihu.com/people/eric0z)
		- -
	- MyLogseq-原创的笔记-大纲形式
	  collapsed:: true
		- journals-每日速记
		- pages-整理后的笔记
			- MyYuque-原创的文章-Markdown形式
		- assets-所有笔记的附件
	- DONE Logseq的块和Page直接的转换
	  collapsed:: true
		- 找到了插件，[hyrijk/logseq-plugin-block-to-page](https://github.com/hyrijk/logseq-plugin-block-to-page)
		- 但是一直提示安装失败，算了，不搞了
		- 真正需要转换成永久笔记的，就建双链，再来剪切吧
	- 使用杂谈
	  collapsed:: true
		- [[Logseq-从碎片化到体系化]]
		- [[Logseq和Obsidian的配合与对比]]
		- 用右侧的目录来代替左侧的收藏页面，因为目录可以展开、编辑、拖动，而收藏只能点击
		- 把Logseq文件夹用[[syncthing]]和[[Git]]管理起来，前者解决垃圾箱和多设备同步，后者解决版本管理
		- 感觉Logseq真的非常方便研究性学习，在研究一个东西时，过程中遇到的一切问题，搜集到的一切资料，自己的一切想法，都可以很方便的记录在这里
	- 迁移WorkFlowy到Logseq的流程
	  collapsed:: true
		- 直接导出opml的方式
			- 不适合大量的块，超过1000以上就超级卡
		- 批处理方式
			- 1.导出纯文本文件
			- 2.用VSCode正则替换
				- 干掉顶级标题
					- -
				- 二级大纲为二级标题
					- 尚学堂高淇21版java300集 https://www.bilibili.com/video/BV15Z4y137pX?spm_id_from=333.905.b_72656c61746564.3
					- ⽹易公开课华保建⽼师《编译原理》
					- 斯坦福⼤学公开课 ：机器学习课程
					- ⿇省理⼯学院公开课：算法导论
					- 码农翻⾝：计算机基础
					- ⾕歌机器学习课程
					- Android 进阶之旅-欧阳鹏 https://blog.csdn.net/ouyang_peng/category_9261478.html
					- Android架构设计方法、技巧与实践-有心课堂 https://space.bilibili.com/24357250/channel/detail?cid=144041&ctype=0
					- Java进阶训练营-极客大学
					- `^	- `
					- `## `
				- 将三级大纲升级为二级大纲
					- `^	`
					- ``
			- 3.用Obsidian提取二级标题为单独文本
				- -
	- 特色亮点 
	  collapsed:: true
		- 做==PDF阅读和标注==非常棒，可以高亮文字和截图，点击可跳转回原始页码
			- 只是贴的高亮文字，在笔记里面显示的页码太抢眼了，希望可以隐藏掉或自定义样式
		- 完美融合了==大纲和Markdown==，虽然它的Markdown在别的软件打开不是非常完美，但在Logseq里面显示效果真的很好
			- collapsed:: true
			- 其实Markdown可以当做json一样，是笔记工具之间的数据交换格式，但是显示时，完全可以有自己的自定义显示效果，就算Logseq创建的md在Obsidian显示效果不是完美，但也能用了
	- 存在问题 
	  collapsed:: true
		- 简直快累觉不爱了，Logseq的文件数量一多，简直卡的一比
		- 以后的增量笔记，存放在Logseq里面，存量的笔记，就老地方放着吧，懒得折腾了
		- 再次迁移ob到logseq失败，logseq的性能真的是太差了
		- 不是很方便将一个==块快速转换为页面==，就像Notion那样，现在只能剪切粘贴，略显麻烦
		- 分享的网页中，==简书图床不能显示==，阿里云图床可以显示，本地图片可以显示
			- 使用Obsidian的local images插件下载简书图床的图片到本地 #Obsidian插件
			- 然后正则替换一下格式
				- MyLogseq/assets
				- ../assets
		- ==选中文字后添加外链==，不是很方便，不能像内联那样按两下`[`就好了
		- 性能问题
			- Logseq在开发数据库版本了，以后文件增长带来的性能需求不会是问题
		- page和block转换的问题
			- -
	- 怎么做任务管理-journals
	  collapsed:: true
		- Logseq做时间管理
			- 思维导图
				- collapsed:: true
				- ![image.png](image_1638513388051_0.png)
			- 任务状态-5种状态
				- -NOW 当前正在关注或执行的，相当于工作台
					- :LOGBOOK:
						- CLOCK: [2021-12-03 Fri 14:37:49]
						- CLOCK: [2021-12-03 Fri 14:37:51]
						- CLOCK: [2021-12-03 Fri 14:37:53]
						- CLOCK: [2021-12-03 Fri 14:37:58]
						- CLOCK: [2021-12-03 Fri 14:38:04]
						- :END:
				- -LATER 稍后准备做的，相当于下一步行动
				- -DONE 已完成的任务
				- -WAITING 等待时机，将来也许要做，远期目标
				- -CANCELLED 暂时搁置的任务，备忘录
			- 任务优先级 /ABC
				- DONE [#A] 任务1
					- :LOGBOOK:
						- CLOCK: [2021-12-03 Fri 14:48:37]--[2021-12-08 Wed 10:14:41] =>  115:26:04
						- :END:
				- DONE [#B] 任务2
					- :LOGBOOK:
						- CLOCK: [2021-12-03 Fri 14:48:56]--[2021-12-08 Wed 10:15:25] =>  115:26:29
						- :END:
				- DONE [#C] 任务3
					- :LOGBOOK:
						- CLOCK: [2021-12-03 Fri 14:49:14]--[2021-12-08 Wed 10:15:29] =>  115:26:15
						- :END:
			- 任务的日程表
				- collapsed:: true
				- DONE 任务11
					- SCHEDULED: <2021-12-05 Sun>
						- :LOGBOOK:
						- CLOCK: [2021-12-03 Fri 15:00:44]
						- CLOCK: [2021-12-03 Fri 15:00:57]
						- :END:
				- 参考
			- 打造一个英文内容权威站，月PV达 10K，月盈利达 $500
			- 参加五次头马活动并至少演讲一次，发表3篇英文文章
			- 2021-OKR-O3-KRs
				- 被动收入投资组合年复合收益率超 15%
			- 2021-OKR-O4-KRs
				- 在博客技术与投资领域分别输出超过10篇文章
			- 由KR来聚拢TASK
				- ![image.png](image_1638516246874_0.png)
			- -
		- Now
		- Later
	- 怎么做笔记管理-pages
	- 怎么做附件管理-assets
	  collapsed:: true
		- Logseq做文件管理
		  collapsed:: true
			- 直接拖动
			- /Users/yutianran/Documents/待处理md/使用Teambition进行团队任务管理.md
			- file:///Users/yutianran/Documents/%E5%BE%85%E5%A4%84%E7%90%86md/%E4%BD%BF%E7%94%A8Teambition%E8%BF%9B%E8%A1%8C%E5%9B%A2%E9%98%9F%E4%BB%BB%E5%8A%A1%E7%AE%A1%E7%90%86.md
			- -
	- 怎么分享自己写的Logseq笔记
	  collapsed:: true
		- Logseq发布
			- Logseq发布流程
				- 1. 标记页面为public:: true
				- 2. 导出图谱-Export public pages，选择路径为MyPKM-Publish
				- 3. 打开SourceTree，提交+推送到Github Pages仓库，它的上传有点慢，可能需要2-3分钟，稍等一下就好
			- 遇到问题
				- 1. 上传到github.io的速度有点慢，不知道是不是自己网络问题
				- 2. 本地可以查看图床，发布出去的网页却没法查看图床了，奇怪
					- 不是所有外链图片都不显示，只有简书的才不显示，阿里云可以显示
					- 有没有可以自动下载Markdown的网络图片并替换为本地图片的插件？
						- pic-migrater [利用PicGo快速迁移Weibo外链图片到GitHub - Pockies | 博客](https://pockies.github.io/2019/04/27/weibo-to-github/)
						- 其实自己写一个python脚本来处理也可以 [利用PicGo快速迁移Weibo外链图片到GitHub - Pockies | 博客](https://pockies.github.io/2019/04/27/weibo-to-github/)
				- 3.
		- -
	- 怎么和其它软件联动
	  collapsed:: true
		- #Finder 系统文件管理
		- #Obsidian md各种复杂的管理
		- #Typora md所见即所得编辑
		- #Zotero 文献管理
		- #Syncthing 多设备同步
		- #git 版本管理
		- https://www.jianguoyun.com/p/DRYUXb0Qhs-VChijm6YE
		- 大纲编辑
		- #pCloud 增量备份网盘
		- #飞书 速记，随时添加想法
		- #滴答清单 任务管理，随时添加任务
	- 自带的特色功能
	- 案例收藏
	  collapsed:: true
		- Logseq的三种使用场景
	- 重要资料
	  collapsed:: true
		- [Logseq-官网](https://logseq.com/)
		- [Logseq-中文社区](https://cn.logseq.com/categories)
		- [Logseq-Github下载地址](https://github.com/logseq/logseq/releases)
		- [Logseq 系列教程-FinnYan](https://www.finncode.cn/logseq/#/page/1.1%20%E5%85%B3%E4%BA%8E%20Logseq)
		- HomePage: https://logseq.com/
		  collapsed:: true
			- Github: https://github.com/logseq/logseq
				- 英文 Discord: https://discord.com/invite/KpN4eHY
				- 中文 Discord: https://discord.com/invite/SVmDc9xvQV
				- Roadmap: https://trello.com/b/8txSM12G/logseq-roadmap
				- 论坛： https://discuss.logseq.com/ & https://cn.logseq.com/
		- [分享:使用logseq + gitee发布的页面，内含教程 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1396)
		- [使用 logseq 部署个人页面](https://dale502.gitee.io/logseq-learn/#/page/%E4%BD%BF%E7%94%A8%20logseq%20%E9%83%A8%E7%BD%B2%E4%B8%AA%E4%BA%BA%E9%A1%B5%E9%9D%A2)
		- [logseq-learn-Contents](https://dale502.gitee.io/logseq-learn/#/page/contents)
	- 其它收藏
	  collapsed:: true
		- [logseq/logseq-plugin-samples: Logseq plugin samples for beginner 🌱](https://github.com/logseq/logseq-plugin-samples)
		- [App+1 | 卡片笔记纷至沓来，Logseq 凭何在我眼中独树一帜？ - 少数派](https://sspai.com/post/68459)
		- [logseq/logseq: A privacy-first, open-source platform for knowledge management and collaboration. Desktop app download link: https://github.com/logseq/logseq/releases, roadmap: https://trello.com/b/8txSM12G/roadmap](https://github.com/logseq/logseq)
	- Logseq的标签和双链很像啊，都会自动生成一个标签的页面
	- /Logseq]]中的标签和双链，本质上是一样的，底层的数据结构其实没有区别的
	- logseq快捷键
	  collapsed:: true
		- dsfa
		- DONE 快速搜索/新建笔记 cmd+K
			- :LOGBOOK:
				- CLOCK: [2021-12-02 Thu 20:30:47]--[2021-12-02 Thu 20:30:49] =>  00:00:02
				- CLOCK: [2021-12-02 Thu 20:31:00]--[2021-12-02 Thu 20:31:40] =>  00:00:40
				- :END:
	- logseq的大纲配合obsidian的 [[MarkDown]] ，简直就是完美配合
	- [[双链笔记]]
	  collapsed:: true
		- 特色亮点
			- [[每日记录]]
			- 自生成的关键词页面
			- 文末自动的双向链接和未关联引用的提示
			- 直观的关系图概览
			- 侧边栏查阅
			- 段落级的版本控制
			- 这些功能都为我们笔记的[[随时记录]]与[[自动化整理]]提供了极大的便利。
		- [[每日``笔记]]
		  collapsed:: true
			- 日常在每日笔记记录每日的行动日志
			- 做了什么，做到第几步了，遇到了什么问题，找到了什么解决方案，都可以随手记录在这里
			- 一些突然的想法，不方便给微信的Cubox发消息，也可以记录到这里
		- [[卡片笔记]]
			- 区别对每日笔记里面的随手记录，主要就是一些略微整理了的笔记
			- 多整理一些[[名词]]性的卡片，多使用[[别名]]，以方便让软件给我们[[推荐]]双链
		- [[文章笔记]]
			- 一般是作为比较正式的[[分享]]，可以发布到[[语雀]]作为[[知识库]]存档的，非常喜欢语雀的阅读界面，左侧书籍目录 ，右侧文章内部目录
				- 具体流程，参见[[如何同步本地Markdown文件夹到语雀]]
			- 其实也不是所有的[[分享]]都要那么正式，Logseq]]的[[大纲]]分享出去，阅读效果也挺好的
				- 具体流程，参见[[如何分享Logseq大纲到Gitee Pages]]
	- 使用Logseq，最重要的是，从今天开始记录，而不是迁移以往的笔记
	- 不要在Logseq上看PDF了，还是用iPad看方便一点
	- 补充一下,如果你修改了首页，然后想在首页上添加一个所有日记的链接，可以添加这一行代码到你首页的那个页面里：[:a {:href "/all-journals"} "所有日记"]
	- 高级搜索
	  collapsed:: true
		- 不建议新手去折腾高级搜索
	- 插件
	  collapsed:: true
		- 不建议新手去折腾插件，因为Logseq本身提供的功能已经足以满足我们的大多数笔记场景
		- 不过这几个插件强烈建议安装一下
		  collapsed:: true
			- 只建议安装我现在依然启用的那几个
				- ![](https://photo.fishyer.com/img/202204231748406.png)
		-
- 04-收集资料
	- 集锦-成体系的专栏、文档、书籍、视频
		- [Logseq官方帮助文档](https://docs.logseq.com/#/page/Contents)
		- [Logseq 中文文档](https://logseq-documents-cn.fishyer.com/#/page/Contents)
		  collapsed:: true
			- 来源于[Logseq 中文文档 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1787)
			- 我怕他删库了，所以自己备份到自己服务器，重新部署了一份
		- [Logseq从入门到精通-15集视频-bilibili](https://www.bilibili.com/video/BV1144y14764)
		  collapsed:: true
			- 来源自Obsidan群的 #及时春雨
	- 文章-不超过10篇，强烈建议看看的
		- [Logseq小白系列教程入门篇一 - 知乎](https://zhuanlan.zhihu.com/p/343854552)
		- [Logseq小白系列教程入门篇二 - 知乎](https://zhuanlan.zhihu.com/p/405764984)
		- [OKR + GTD + Note => Logseq · 构建我的被动收入](https://www.bmpi.dev/self/okr-gtd-note-logseq/)
		- [使用Logseq构建GTD系统 - samwei12 - 博客园](https://www.cnblogs.com/samwei12/p/shi-yonglogseq-gou-jiangtd-xi-tong.html)
	- 其它-所有相关文章，多多益善
		- [Quicker + zotero/Mdnotes 实现Logseq打开外部PDF并注释 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/1446)
		- [如何发布logseq成为博客 - 知乎](https://zhuanlan.zhihu.com/p/344165645)
		- [logseq/awesome-logseq: Awesome Logseq resources created by the community <3](https://github.com/logseq/awesome-logseq)
		- [Logseq使用教程之七：Telegram+IFTTT+Quicker实现Logseq速记 - 分享 - Logseq 中文社区](https://cn.logseq.com/t/topic/3369)
		- [logseq使用经验分享](https://xutuan.vercel.app/#/page/logseq%E4%BD%BF%E7%94%A8%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB)
- {{embed [[欢迎加入]]}}
-