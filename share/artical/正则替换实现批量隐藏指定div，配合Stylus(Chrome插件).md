---
date: 2022-04-27T02:21:37+08:00
title: 正则替换实现批量隐藏指定div，配合Stylus(Chrome插件)
---

# 正则替换实现批量隐藏指定div，配合Stylus(Chrome插件)

## 目的
  - 实现指定网站的阅读页面优化

## 工具和资源
  - 编辑工具-Sublime
  - 正则表达式在线测试 | 菜鸟工具
    - https://c.runoob.com/front-end/854/
## 网站效果图
  - 替换前
![](https://yupic.oss-cn-shanghai.aliyuncs.com/20211029203048.png)

  - 替换后
![](https://yupic.oss-cn-shanghai.aliyuncs.com/20211029203059.png)
## 实现说明
  - 表达式

![](https://yupic.oss-cn-shanghai.aliyuncs.com/20211029202943.png)

  - 替换前
    - 
  - 替换后
    - 
### Find说明
  - 代码
    - ^([.#].*[A-Za-z])$
  - ^表示开头
  - $表示结尾
  - ()表示匹配到的文本，用于在Replace中使用 $1
### Replace说明
  - 代码
    "$1 {
        display: none;
    }"
  - $1 表示匹配到的第一个元素，插入到替换后的文本里面