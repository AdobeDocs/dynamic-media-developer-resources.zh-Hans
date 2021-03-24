---
description: 通过将图层来源(来源=)与背景图层来源对齐在pos=指定的偏移处来定位图层。
solution: Experience Manager
title: 图层放置
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# 图层放置{#layer-placement}

通过将图层来源(来源=)与背景图层来源对齐在pos=指定的偏移处来定位图层。

如果未显式指定图像图层的图层来源，则按如下方式计算：

1. 确定图像锚点。 使用`anchor=`，或者（如果未指定）`catalog::Anchor`。
1. 如果定义了图像锚点，则应用图层变换并`extend=`将其转换为来源=值。
1. 如果未定义图像锚点，则图层来源将放置在图层矩形的中心（应用`extend=`之后）。

![](assets/layerplacement.png)

