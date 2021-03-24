---
description: 颜色转换渲染方法。 在未使用icc=指定渲染方法时，为颜色转换提供默认渲染方法。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# IccRenderIntent{#iccrenderintent}

颜色转换渲染方法。 在未使用icc=指定渲染方法时，为颜色转换提供默认渲染方法。

## 属性 {#section-2540099fb2fc47d29b04642da4f5922a}

枚举。 设置为0表示感知，设置为1表示相对比色，设置为2表示饱和度，设置为3表示绝对比色。

## 默认 {#section-61a05067905b44099c228e15de279dbd}

如果未定义或为空，则从`default::IccRenderIntent`继承。

## 另请参阅 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute:::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *,  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
