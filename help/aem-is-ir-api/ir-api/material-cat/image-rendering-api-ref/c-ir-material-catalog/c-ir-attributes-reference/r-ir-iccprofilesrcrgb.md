---
title: IccProfileSrcRgb
description: RGB預設輸入色彩設定檔。 指定用於RGB材質影像和未嵌入色彩設定檔的暈映的ICC色彩設定檔名稱。 也適用於RGB色彩值，以各種影像演算指令指定，例如bgc=和color=。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB預設輸入色彩設定檔。 指定用於RGB材質影像和未嵌入色彩設定檔的暈映的ICC色彩設定檔名稱。 也用於使用各種「影像演算」指令指定的RGB色彩值，例如 `bgc=` 和 `color=`.

## 屬性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文字字串。 若指定，則必須為有效 `icc::Name` 值來自此影像目錄或預設目錄的ICC設定檔對映，或是相對於的檔案路徑 `attribute::RootPath`. 參考的ICC設定檔必須是RGB設定檔。

## 默认 {#section-0171cd6680284bfa9844b9cc3644ca61}

繼承自 `default::IccProfileSrcRgb` 如果未定義或為空。 若 `attribute::IccProfileSrcRgb` 無法解析為有效的設定檔， `attribute::IccProfileRgb` 會改用。

## 另请参阅 {#section-1ba91666830f4c209c39260ea29f938e}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [attribute：：IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
