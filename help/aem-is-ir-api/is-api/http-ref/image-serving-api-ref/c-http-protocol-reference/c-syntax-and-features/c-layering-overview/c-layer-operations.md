---
description: 除了相对于图层0调整大小(size=)和定位(pos=)图层，以及使用layer=命令指定合成顺序（z顺序）外，还可以旋转(rotate=)和翻转(flip=)图层。
seo-description: 除了相对于图层0调整大小(size=)和定位(pos=)图层，以及使用layer=命令指定合成顺序（z顺序）外，还可以旋转(rotate=)和翻转(flip=)图层。
seo-title: 图层操作
solution: Experience Manager
title: 图层操作
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 层操作{#layer-operations}

除了相对于图层0调整大小(size=)和定位(pos=)图层，以及使用layer=命令指定合成顺序（z顺序）外，还可以旋转(rotate=)和翻转(flip=)图层。

当在模板中动态更改图像或文本时，`origin=`和`anchor=`属性可用于保持图层之间的所需对齐。

`maskUse=`命令可用于图像图层访问具有单独遮罩的图像的背景区域。

`opac=` 可用于改变图层的不透明度，以 `hide=` 及显示或隐藏图层。
