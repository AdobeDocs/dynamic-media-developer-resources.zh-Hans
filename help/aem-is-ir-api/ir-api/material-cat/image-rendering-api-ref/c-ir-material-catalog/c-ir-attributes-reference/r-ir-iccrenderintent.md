---
title: IccRenderIntent
description: 颜色转换渲染意图。 在未使用icc=指定渲染意图时，为颜色转换提供默认渲染意图。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

颜色转换渲染意图。 在未指定渲染意图时，为颜色转换提供默认的渲染意图 `icc=`.

## 属性 {#section-0a38c60e1525426185616c42824aee2c}

枚举。 对于感知度，设置为0；对于相对比色，设置为1；对于饱和度，设置为2；对于绝对比色，设置为3。 将留空或设置为任何其他值，以使用颜色配置文件中定义的默认渲染意图。

## 默认 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

继承自 `default::IccRenderIntent`如果未定义。 如果为空，则应用“相对比色”。

## 另请参阅 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[属性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [属性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
