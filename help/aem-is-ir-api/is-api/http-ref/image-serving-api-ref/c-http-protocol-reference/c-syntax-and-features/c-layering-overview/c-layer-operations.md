---
description: 除了相对于图层0调整大小(size=)和定位(pos=)图层并使用layer=命令指定合成顺序（z顺序）之外，还可以旋转(rotate=)和翻转(flip=)图层。
solution: Experience Manager
title: 图层操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 图层操作{#layer-operations}

除了相对于图层0调整大小(size=)和定位(pos=)图层并使用layer=命令指定合成顺序（z顺序）之外，还可以旋转(rotate=)和翻转(flip=)图层。

在模板中动态更改图像或文本时，`origin=`和`anchor=`属性可用于在图层之间保持所需的对齐方式。

`maskUse=`命令可用于图像图层，以访问具有单独蒙版的图像的背景区域。

`opac=`可用于更改图层不透明度，`hide=`可用于显示或隐藏图层。
