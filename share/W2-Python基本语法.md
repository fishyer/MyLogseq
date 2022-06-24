- 第2期课程更新完毕，希望大家都能在下周日(06-26)之前完成作业，每个人都能写出一个简单的程序。
- 参考资料
	- [Python3 教程 | 菜鸟教程](https://www.runoob.com/python3/python3-tutorial.html)
	- [《Python Cookbook》第三版](file:///D:/Dropbox/MyObsidian/MyAttachment/PythonCookbook-%E7%AC%AC%E4%B8%89%E7%89%88%E4%B8%AD%E6%96%87v3.0.0.pdf)
	- [Python编程快速上手—让繁琐工作自动化 PDF中文高清晰完整版](file:///D:/Dropbox/MyObsidian/MyAttachment/MyZotoreFile/Python%E7%BC%96%E7%A8%8B%E5%BF%AB%E9%80%9F%E4%B8%8A%E6%89%8B%E2%80%94%E8%AE%A9%E7%B9%81%E7%90%90%E5%B7%A5%E4%BD%9C%E8%87%AA%E5%8A%A8%E5%8C%96.pdf)
- 本期作业
	- 1-使用循环实现一个求和函数，计算sum(10)，预期输出55
	  collapsed:: true
		- 答案
			- ```python
			  def sum(n):
			      result=0
			      for i in range(n+1):
			          result=result+i
			      return result
			  sum(10)
			  ```
	- 2-使用递归实现一个求和函数，计算sum(10)，预期输出55
	  collapsed:: true
		- 答案
			- ```python
			  def sum2(n):
			      if n==1:
			          return 1
			      return n+sum2(n-1)
			  sum2(10)
			  ```
	- 3-输入一个文件夹路径，可以打印出文件夹的所有子文件（不包含嵌套的子文件夹）
	  collapsed:: true
		- 答案
			- ```python
			  import os
			  
			  dir = input('请输入一个目录：')
			  # dir=r"C:\Users\Administrator\Desktop\jupyter\testDir" #加r防止转义
			  
			  #获取目录列表
			  list_dir = os.listdir(dir)
			  #打印目录列表
			  print(list_dir)
			  #遍历目录列表
			  for temp in list_dir:
			      print(temp)
			  ```
	- 4-输入一个文件夹路径，可以打印出文件夹的所有子文件（包含嵌套的子文件夹）
	  collapsed:: true
		- ```python
		  import os
		  
		  dir = input('请输入一个目录：')
		  # dir=r"C:\Users\Administrator\Desktop\jupyter\testDir" #加r防止转义
		  
		  def traverseFolder(dirPath):
		      #获取目录列表
		      listDir = os.listdir(dirPath)
		      #遍历目录列表
		      for path in listDir:
		          fullPath=os.path.join(dirPath,path)
		          # 是文件夹的话，就先打印文件夹的名称，再去遍历这个子文件夹
		          if os.path.isdir(fullPath):
		              print(fullPath)
		              traverseFolder(fullPath)
		          # 是文件的话，直接打印就好了
		          else:
		              print(fullPath)
		  
		  traverseFolder(dir)
		  print(dir)
		  ```
	- 测试的文件夹，可以直接就用[[百度网盘群]]里的testDir即可。还有一些python学习书籍，我也上传到网盘群了
- 本期大纲
	- [[Python之歌]]
	- 变量
	  collapsed:: true
		- [Python基本语法-变量-数字](https://lusun.com/v/ANLbWYsM30Y)
			- 数字
			  collapsed:: true
				- int 1 2 3
				- float 1.2
				- 加减乘除
		- [Python基本语法-变量-字符串](https://lusun.com/v/P2QpWSc15ac)
			- string-字符串 “test”
			  collapsed:: true
				- split-分割
				- join-合并
				- replace-替换
				- strip-去除空格
				- 索引 [0] [1] [-1] [-2] [1:]
					- ：是前闭后开
				- 类型转换
					- ```python
					  str="123"
					  toInt=int(str)
					  toStr=str(toInt)
					  ```
				- 查看类型 type
					- `type(toStr)`
				- id(a) 查看变量a的内存地址
		- [Python基本语法-变量-列表](https://lusun.com/v/hbnWEERKftK)
			- list-列表 [1,2]
			  collapsed:: true
				- 不限子类型 a=[1,"hello",2.5]
				- 嵌套 b=[2,b]
				- 是否包含 2 in b
				- 取值 a[1]
				- 添加 a.append("test")
				- 删除 a.remove("test)
				- 排序
					- sort-直接原地排序
					- sorted-创建新的
		- [Python基本语法-变量-字典](https://lusun.com/v/Vb2GysPRpvb)
			- dict-字典 {key1:value2,key2:value2}
			  collapsed:: true
				- 查询 dict['testKey']
				- 赋值 dict['testKey']='testValue'
				- 字典无序
				- 判断是否存在key
		- [Python基本语法-变量-集合](https://lusun.com/v/lBW6AWka3V2)
			- set-集合 {1,1,1,2,3,3,4}
			  collapsed:: true
				- 自带去重
				- 并集-a.union(b)  a∣b
				- 交集-a.intersection(b) a&b
				- 差集-a.difference(b) a有b没有 a-b
				- 子集-a.issubset(b)  a是否是b的子集 a <= b
	- [Python基本语法-判断结构](https://lusun.com/v/92jUh4v8Mnm)
		- 判断结构 if
		  collapsed:: true
			- ```python
			  test= 67
			  if test>80:
			      print("良好")
			  elif test>60:
			      print("及格")
			  else:
			      print("不及格")
			  ```
	- [Python基本语法-循环结构](https://lusun.com/v/ylf7V17Gszc)
		- 循环结构 for
		  collapsed:: true
			- for循环
				- ```python
				  a=[1,3,5,7]
				  for i in a:
				      print(i)
				  ```
				- ```python
				  for i in range(10):
				      print(i)
				  ```
			- while循环
				- ```python
				  s=set([12,4,6,8])
				  while s:
				      p=s.pop()
				      print(p)
				  ```
			- continue 跳过本次循环
				- ```python
				  list=[1,2,3,4]
				  for i in list:
				      print("进入",i)
				      if i%2 == 0:
				          print(i)
				      else:
				          continue
				      print("退出",i)
				  ```
			- break 跳出所有循环
				- ```python
				  list=[1,2,3,4]
				  for i in list:
				      print("进入",i)
				      if i%2 == 0:
				          print(i)
				      else:
				          break
				      print("退出",i)
				  ```
			- return 跳出方法，下面讲到函数的时候会用到
	- [Python基本语法-函数](https://lusun.com/v/ifobvman4EI)
		- 函数 def
		  collapsed:: true
			- 简单函数
				- ```python
				  def add(a,b):
				      print("a=",a)
				      print("b=",b)
				      return a+b
				  add(5,6)
				  ```
			- 默认参数
			  collapsed:: true
				- ```python
				  def add(a=2,b=3):
				      print("a=",a)
				      print("b=",b)
				      return a+b
				  add(b=6)
				  ```
			- 递归函数，函数里面自己调用自己
				- ```python
				  def sum(n):
				      if n==1:
				          return 1
				      return n+sum(n-1)
				  sum(10)
				  ```
	- 第三方模块 import
		- [Python基本语法-文件操作](https://lusun.com/v/obXFyRYes4r)
			- 文件操作 os
				- 获取本地文件夹的目录
		- 网络操作 requests
		- 日期时间 time datetime
		- pandas
		- lxml