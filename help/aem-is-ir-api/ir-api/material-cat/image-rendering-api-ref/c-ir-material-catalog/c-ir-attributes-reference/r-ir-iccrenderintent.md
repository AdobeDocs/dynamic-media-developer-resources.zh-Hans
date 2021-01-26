---
description: 颜色转换渲染方法。 在icc=未指定渲染方法时，提供颜色转换的默认渲染方法。
seo-description: 颜色转换渲染方法。 在icc=未指定渲染方法时，提供颜色转换的默认渲染方法。
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

颜色转换渲染方法。 在icc=未指定渲染方法时，提供颜色转换的默认渲染方法。

## 属性 {#section-0a38c60e1525426185616c42824aee2c}

枚举。 对于感知，设置为0；对于相对比色，设置为1；对于饱和度，设置为2；对于绝对比色，设置为3。 保留为空或设置为任何其他值，以使用在颜色用户档案中定义的默认渲染方法。

## 默认 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

从`default::IccRenderIntent`继承（如果未定义）。 如果为空，则应用“相对比色”。

## 另请参阅 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[属性：:IccProfile](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) *, [属性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
