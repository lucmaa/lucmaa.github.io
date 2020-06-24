---
title: ARB_texture_view
date: 2020-06-09 12:17:07
tags:
---

# 概述
ARB_texture_view是ARB Extension #124. 它主要实现两种纹理对象的操作：
- 它可以以不同的像素格式或数据类型(format/type)解释同一个纹理对象存储在内存中的数据(data store)
- 它可以抽取已有纹理对象某个范围的Mipmap Levels或Array Slices作为一个新纹理对象

注意: 第二种功能的抽取是引用，而不是内存拷贝。

从以上两点可以看出，ARB_texture_view的主要目标就是只增加对已有纹理数据的引用(视图)，而不上传纹理数据.
因为向GPU上传纹理数据是既费时又耗显存的操作。

没有增加新的纹理类型，原来的纹理对象被划分为以下几个部分: