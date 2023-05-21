---
title: IccProfileSrcCmyk
description: CMYK預設輸入色彩設定檔。 指定用於未嵌入色彩設定檔之CMYK材質影像的ICC色彩設定檔名稱。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK預設輸入色彩設定檔。 指定用於未嵌入色彩設定檔之CMYK材質影像的ICC色彩設定檔名稱。

## 屬性 {#section-0cee77438d914c319ec876edb3490821}

文字字串。 若指定，則必須為有效 `icc::Name` 值來自此影像目錄或預設目錄的ICC設定檔對映，或是相對於的檔案路徑 `attribute::RootPath`. 參照的ICC設定檔必須是CMYK設定檔。

## 默认 {#section-11f6239e0dd14827abf4a95c1b30161c}

繼承自 `default::IccProfileSrcCmyk` 如果未定義或為空。 若 `attribute::IccProfileSrcCmyk` 無法解析為有效的設定檔， `attribute::IccProfileCmyk` 會改用。

## 另请参阅 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [屬性：：IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
