---
description: 除了相对于层0的大小调整(size=)和定位(pos=)层以及使用layer=命令指定复合顺序（z阶）外，层还可以旋转(rotate=)和翻转(flip=)。
solution: Experience Manager
title: 层操作
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# 层操作{#layer-operations}

除了相对于层0的大小调整(size=)和定位(pos=)层以及使用layer=命令指定复合顺序（z阶）外，层还可以旋转(rotate=)和翻转(flip=)。

当模板中的图像或文本发生动态更改时，`origin=`和`anchor=`属性可用于保持图层之间的所需对齐方式。

`maskUse=`命令可用于图像层访问具有单独掩码的图像的背景区域。

`opac=` 可用于更改图层的不透明度，以 `hide=` 及显示或隐藏图层。
