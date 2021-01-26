---
description: 大多数材料都可以动态着色。
seo-description: 大多数材料都可以动态着色。
seo-title: 着色材料
solution: Experience Manager
title: 着色材料
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

着色算法简单易行，对色调范围有限的材料图像效果最好。 要对材料着色，渲染器只需减去`bgc=`值，并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用着色。 `bgc=` 被橱柜材料忽视；而是使用嵌入在文件 [!DNL vnc] 中的基色值。
