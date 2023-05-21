---
title: IccRenderIntent
description: 色彩轉換演算色彩比對方式。 當未以icc=指定色彩演算比對方式時，提供預設色彩演算比對方式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

色彩轉換演算色彩比對方式。 提供預設色彩演算比對方式，以便在未指定色彩演算比對方式時進行色彩轉換。 `icc=`.

## 屬性 {#section-0a38c60e1525426185616c42824aee2c}

列舉。 設為0代表可感知、1代表相對比色、2代表飽和度、3代表絕對比色。 請保持空白或設定為任何其他值，以使用顏色設定檔中定義的預設色彩演算比對方式。

## 默认 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

繼承自 `default::IccRenderIntent`若未定義。 如果為空，則套用「相對比色」。

## 另请参阅 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ， [屬性：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)， [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
