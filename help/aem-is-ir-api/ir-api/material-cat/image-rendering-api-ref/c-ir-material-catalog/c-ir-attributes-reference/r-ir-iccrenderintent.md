---
title: IccRenderIntent
description: 颜色转换调色。 如果未使用“icc=”指定渲染方法，则它提供颜色转换的默认渲染方法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

颜色转换调色。 如果未使用`icc=`指定渲染方法，则为颜色转换提供默认渲染方法。

## 属性 {#section-0a38c60e1525426185616c42824aee2c}

枚举。 设置为0表示可感知，1表示相对比色，2表示饱和度，3表示绝对比色。 保持空或设置为任何其他值，以便可以使用颜色配置文件中定义的默认调色。

## 默认 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

如果未定义，则从`default::IccRenderIntent`继承。 如果为空，则应用“相对比色”。

## 另请参阅 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)，[attribute：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)，[`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
