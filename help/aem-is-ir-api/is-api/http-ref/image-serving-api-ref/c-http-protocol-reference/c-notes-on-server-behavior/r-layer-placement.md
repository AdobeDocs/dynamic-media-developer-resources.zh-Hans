---
description: 通过将层来源(来源=)与背景层来源对齐在pos=指定的偏移处来定位层。
seo-description: 通过将层来源(来源=)与背景层来源对齐在pos=指定的偏移处来定位层。
seo-title: 图层放置
solution: Experience Manager
title: 图层放置
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 图层放置{#layer-placement}

通过将层来源(来源=)与背景层来源对齐在pos=指定的偏移处来定位层。

如果未为图像图层显式指定图层来源，则按如下方式计算该图层：

1. 确定图像锚点。 使用`anchor=`，或者，如果未指定，则使用`catalog::Anchor`。
1. 如果定义了图像锚点，则应用图层变换并`extend=`将其转换为来源=值。
1. 如果未定义图像锚点，则图层来源将放置在图层矩形的中心（应用`extend=`后）。

![](assets/layerplacement.png)

