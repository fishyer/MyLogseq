- 题外话
  collapsed:: true
	- 不好意思，最近因为个人事情比较繁杂，所以有两周没有录制，计划以后有时间了再来补
	- 另一方面呢，希望大家能积极的给我一点反馈，无论是视频的观看人数，还是群里的交流反馈，都不太良好，感觉都没啥人看，老实说，有点觉得自己做的事情好像没啥意义，没有太大的动力做下去了
- 参考资料
	- [Python3 File 方法 | 菜鸟教程](https://www.runoob.com/python3/python3-file-methods.html)
	- [Python3 OS 文件/目录方法 | 菜鸟教程](https://www.runoob.com/python3/python3-os-file-methods.html)
	- [Python常用模块os和shutil学习 - 掘金](https://juejin.cn/post/6997047326711742494)
	-
- 本期视频
	- [W3-Python文件操作](https://lusun.com/v/22OHhmRF7RG)
- 本期作业
	- 文件批量重命名，加上“python-”的前缀
	- 生成一份目录文件-md
-
- 本期大纲
	- 批量操作文件
		- 文件重命名
		- 文件批量移动
		- 文件去重
		- ```python
		  # 批量操作文件
		  import os,shutil
		  
		  # dir = input('请输入一个目录：')
		  dir=r"D:\BaiduDown\testDir01\testDir" #加r防止转义
		  
		  destDir=r"D:\BaiduDown\testDir01\collect-md"
		  
		  visited=set()
		  
		  content=""
		  
		  def processFile(path):
		      oldPathName=os.path.splitext(os.path.basename(path))[0]
		      dirName=os.path.dirname(path)
		      extName=os.path.splitext(path)[1]
		      baseName=os.path.basename(path)
		  #     newPathName="python-"+oldPathName
		  #     newPath=os.path.join(dirName,newPathName+extName)
		  #     print(f"{oldPathName}->{newPath}")
		  #     os.rename(path,newPath)
		  #     print(path,extName)
		  #     if extName==".md":
		  #         print(f"{path}->{destDir}")
		  #         shutil.move(path,destDir)
		  #     if baseName in visited:
		  #         os.remove(path)
		  #         print(f"{path}->删除")
		  #     else:
		  #         print(f"{path}->标记")
		  #         visited.add(baseName)
		      global content
		      link=path.replace("\\","/")
		      content=content+f"- [{baseName}](file:///{link})\n"
		  
		  def traverseFolderWithProcess(dirPath):
		      #获取目录列表
		      listDir = os.listdir(dirPath)
		      #遍历目录列表
		      for path in listDir:
		          fullPath=os.path.join(dirPath,path)
		          # 是文件夹的话，就先打印文件夹的名称，再去遍历这个子文件夹
		          if os.path.isdir(fullPath):
		  #             processFile(fullPath)
		              traverseFolderWithProcess(fullPath)
		          # 是文件的话，直接打印就好了
		          else:
		              processFile(fullPath)
		  
		  traverseFolderWithProcess(dir)
		  path=r"D:\BaiduDown\testDir01\testDir\out-file.md"
		  writeFile(content,path)
		  # processFile(r"D:\BaiduDown\testDir\dir01\dir1-file1.txt")
		  ```
	- 获取文件路径信息
		- ```python
		  import os
		  
		  # 获取文件路径信息
		  def printPath(path):  
		      print(path)
		      print(os.path.dirname(path), ".dir")
		      print(os.path.basename(path), ".basename")
		      print(os.path.splitext(path)[0], ".stem")
		      print(os.path.splitext(path)[1], ".ext")
		      print(os.path.splitext(os.path.basename(path))[0])
		  
		  path=r"D:\BaiduDown\testDir\file04.txt"
		  printPath(path)
		  ```
	- 读取文件
		- ```python
		  # 读取文件
		  def readFile(path):  
		      str = ""
		      with open(path, 'r', encoding='utf-8') as file:
		          str = file.read()
		      print(f"读取文件成功：{path}")
		      return str
		  
		  path=r"D:\BaiduDown\testDir\file04.txt"
		  content=readFile(path)
		  print(content)
		  ```
	- 写入文件
		- ```python
		  # 写入文件
		  def writeFile(val, path):  
		      if os.path.exists(path):
		          os.remove(path)
		      with open(path, 'w', encoding='utf-8') as file:
		          file.write(val)
		          print(f"写入文件成功：{path}")
		  
		  str="这是写入到文件里面的内容"
		  path=r"D:\BaiduDown\testDir\file04.txt"
		  writeFile(str,path)
		  ```
		- 输出的目录文件示例：
			- `[dir1-file1.txt](file:///D:/BaiduDown/testDir01/testDir/dir01/dir1-file1.txt)`
			- [dir1-file1.txt](file:///D:/BaiduDown/testDir01/testDir/dir01/dir1-file1.txt)
			- [file01.txt](file:///D:/BaiduDown/testDir01/testDir/dir01/file01.txt)
			- [file03.txt](file:///D:/BaiduDown/testDir01/testDir/dir01/file03.txt)
			- [dir2-file1.txt](file:///D:/BaiduDown/testDir01/testDir/dir02/dir2-file1.txt)
			- [out-file.md](file:///D:/BaiduDown/testDir01/testDir/out-file.md)
			- [out-file.txt](file:///D:/BaiduDown/testDir01/testDir/out-file.txt)
	-
-