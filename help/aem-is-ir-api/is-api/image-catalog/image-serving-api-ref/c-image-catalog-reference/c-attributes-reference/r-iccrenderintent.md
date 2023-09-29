---
title: IccRenderIntent
description: 颜色转换调色。 当没有为调色指定“icc=”时，它为颜色转换提供默认的调色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

颜色转换调色。 如果未通过指定渲染方法，则为颜色转换提供默认渲染方法 `icc=`.

## 属性 {#section-2540099fb2fc47d29b04642da4f5922a}

枚举。 设置为0表示可感知，1表示相对比色，2表示饱和度，3表示绝对比色。

## 默认 {#section-61a05067905b44099c228e15de279dbd}

继承自 `default::IccRenderIntent` 如果未定义或为空。

## 另请参阅 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;， [attribute：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)， [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
