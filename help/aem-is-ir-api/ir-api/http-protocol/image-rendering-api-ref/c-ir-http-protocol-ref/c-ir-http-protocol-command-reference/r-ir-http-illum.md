---
description: 照明图选择器。 指定此材料更喜欢用来渲染的照明映射。
seo-description: 照明图选择器。 指定此材料更喜欢用来渲染的照明映射。
seo-title: illum
solution: Experience Manager
title: illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# illum{#illum}

照明图选择器。 指定此材料更喜欢用来渲染的照明映射。

`illum=-1|0|1|2`

如果指定的照明映射在目标暗角中不可用，则使用最近的可用映射。

`illum=-1` 指定根据值自动选择照明映 `gloss=` 射。

## 属性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材料属性。 如果暗角未定义多个照明映射，则忽略此参数。

## 默认 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另请参阅 {#section-9132e60381c64aa3a8ed1319690db55e}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
