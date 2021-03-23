---
description: 图像锚点。 指定可重复纹理、壁边框或贴花图像的锚点（热点）。
seo-description: 图像锚点。 指定可重复纹理、壁边框或贴花图像的锚点（热点）。
seo-title: 锚点
solution: Experience Manager
title: 锚点
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# 锚点{#anchor}

图像锚点。 指定可重复纹理、壁边框或贴花图像的锚点（热点）。

可重复的纹理应用于晕影对象，以便纹理锚点位于对象的纹理来源点。 倾斜图像被应用到晕影对象，以便倾斜锚点位于对象的倾斜来源点。 对于墙边框，只使用x值；将忽略y值。

## 属性 {#section-bc4bc8b897c64535b88681e57d72942f}

两个整数，以逗号分隔。 相对于图像左上角的像素偏移。 如果`catalog::Alignment=3`和由纯色和机柜材料忽略。

## 默认 {#section-b7ccc419a356415294706cd295ae96c9}

如果字段为空或不存在，则使用可重复纹理材料的图像左上角(0,0)，或在贴花材料的情况下使用图像的中心。

## 另请参阅 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
