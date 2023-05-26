---
title: IccBlackPoint补偿
description: 黑场补偿。 指定在通过icc=未做出明确选择时，是否应将黑场补偿应用于颜色转换。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d075434-5ef0-4b6a-ad24-1ef9c57e3e47
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# IccBlackPoint补偿{#iccblackpointcompensation}

黑场补偿。 指定在没有通过做出明确选择时，是否应将黑场补偿应用于颜色转换 `icc=`.

## 属性 {#section-21fd20b16bea4a22aecab0ae8b81e332}

标记. 设置为 `0` 禁用或 `1` 启用黑场补偿。

## 默认 {#section-5bc6703a43a149f18af88b70baae568f}

继承自 `default::IccBlackPointCompensation` 如果未定义或为空。

## 另请参阅 {#section-90fcbddf02c54846aa09f85fabc7b4d4}

[attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
