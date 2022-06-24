---
date: 2022-04-27T02:21:37+08:00
tags:
- '#说明'
- '#演示图'
title: 8种ScaleType
---

# 8种ScaleType

#演示图
![](https://photo.fishyer.com/img/202204261913878.png)

![](https://photo.fishyer.com/img/202204261914723.png)


![](https://photo.fishyer.com/img/202204261914087.png)
![](https://photo.fishyer.com/img/202204261914452.png)
#说明
1. FIT_XY：对原图宽高进行放缩，该放缩不保持原比例来填充满ImageView。
2. MATRIX：不改变原图大小从ImageView的左上角开始绘制，超过ImageView部分不再显示。
3. CENTER：对原图居中显示，超过ImageView部分不再显示。
4. CENTER_CROP：对原图居中显示后进行等比放缩处理，使原图最小边等于ImageView的相应边。
5. CENTER_INSIDE：若原图宽高小于ImageView宽高，这原图不做处理居中显示，否则按比例放缩原图宽(高)是之等于ImageView的宽(高)。
6. FIT_START：对原图按比例放缩使之等于ImageView的宽高，若原图高大于宽则左对齐否则上对其。
7. FIT_CENTER：对原图按比例放缩使之等于ImageView的宽高使之居中显示。
8. FIT_END：对原图按比例放缩使之等于ImageView的宽高，若原图高大于宽则右对齐否则下对其。

>当我们没有在布局文件中使用scaleType属性或者是没有手动调用setScaleType方法时，那么mScaleType的默认值就是FIT_CENTER。