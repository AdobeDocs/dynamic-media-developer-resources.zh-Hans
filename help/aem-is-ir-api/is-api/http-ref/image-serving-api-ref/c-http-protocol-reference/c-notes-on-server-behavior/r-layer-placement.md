---
title: 图层放置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 图层放置{#layer-placement}

通过使图层原点(origin=)与背景图层原点在由pos=指定的偏移处对齐来定位图层。

如果没有为图像图层明确指定图层原点，则按如下方式计算：

1. 确定图像锚点。 使用 `anchor=`，或者，如果未指定， `catalog::Anchor`.
1. 如果定义了图像锚点，则应用图层转换和 `extend=` 将其转换为origin=值。
1. 如果未定义图像锚点，则图层原点将放置在图层矩形的中心（应用后） `extend=`)。

![图层放置图像](assets/layerplacement.png)
