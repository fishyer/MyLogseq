title:: 添加server.js，部署动态接口到云端

- title:: 添加server.js，部署动态接口到云端
- 添加/api/server.js，注意路径的文件夹一定要是api ,server.js则是可以随便命名的
	- 通过node来启动服务，其实vercel启动服务底层也是用的node
		- node server.js
	- Ctrl+C退出服务
- 获取当前时间并返回给接口
	- 安装库，在直接运行测试代码时会报错，提示找不到module，安装一下就好了
		- npm i moment --save
		- 或
		- yarn add moment
	- 导入库
		- var moment = require('moment');
	- 使用库
		- var current_time = moment(Date.now()).format('YYYY-MM-DD HH:mm:ss')
- 测试代码
	- ```js
	  //导入需要的nodejs库
	  var http = require('http');
	  var moment = require('moment');
	  
	  http.createServer(function (request, response) {
	      //获取当前时间
	      var current_time = moment(Date.now()).format('YYYY-MM-DD HH:mm:ss')
	  
	      // 发送 HTTP 头部 
	      // HTTP 状态值: 200 : OK
	      // 内容类型: text/plain
	      response.writeHead(200, {'Content-Type': 'text/plain'});
	  
	      // 发送响应数据 "Hello Server"
	      response.end("Hello Server "+current_time);
	  }).listen(9001);
	  
	  // 终端打印如下信息
	  console.log('Server running at http://127.0.0.1:9001/');
	  ```