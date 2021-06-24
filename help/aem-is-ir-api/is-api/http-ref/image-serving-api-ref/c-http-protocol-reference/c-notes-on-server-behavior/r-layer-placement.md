---
description: 通过将层原点（原点=）与背景层原点对准在pos=指定的偏移处来定位层。
solution: Experience Manager
title: 图层放置
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# 图层放置{#layer-placement}

通过将层原点（原点=）与背景层原点对准在pos=指定的偏移处来定位层。

如果未为图像层显式指定图层原点，则其计算方式如下：

1. 确定图像锚点。 使用`anchor=`，或者如果未指定，则使用`catalog::Anchor`。
1. 如果定义了图像锚点，请应用层转换并`extend=`将其转换为origin=值。
1. 如果未定义图像锚点，则层原点将放置在层矩形的中心（应用`extend=`后）。

![](assets/layerplacement.png)
