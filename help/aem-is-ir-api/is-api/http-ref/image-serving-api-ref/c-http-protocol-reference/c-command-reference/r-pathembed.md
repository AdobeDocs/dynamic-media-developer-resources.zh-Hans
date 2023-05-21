---
description: 內嵌路徑資料。 指定回應影像中是否應包含來自0層來源影像檔案的Photoshop路徑。
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# pathEmbed{#pathembed}

內嵌路徑資料。 指定回應影像中是否應包含來自0層來源影像檔案的Photoshop路徑。

`pathEmbed=0|1`

## 屬性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

要求屬性。 如果來源影像不包含路徑資料，則忽略。 路徑資料會像影像資料一樣縮放和旋轉。 僅限來自來源影像的路徑 `layer=0` 會處理；會忽略來自其他圖層影像的路徑。

如果輸出影像格式不支援路徑內嵌，則忽略。 請參閱 `fmt=` 以取得支援路徑內嵌的輸出影像格式清單。

## 限制 {#section-697cddb79a1542bc8457d2f4f59eec69}

目前不支援將開放Photoshop路徑（未形成封閉回圈的路徑）嵌入回應影像。

## 默认 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`，不會將路徑內嵌在輸出影像中。

## 另请参阅 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
