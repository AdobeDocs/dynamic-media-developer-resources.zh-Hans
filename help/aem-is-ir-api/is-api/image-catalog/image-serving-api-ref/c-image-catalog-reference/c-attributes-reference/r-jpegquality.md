---
description: 預設JPEG編碼屬性。 指定JPEG回覆影像的預設屬性。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# JpegQuality{#jpegquality}

預設JPEG編碼屬性。 指定JPEG回覆影像的預設屬性。

## 屬性 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整數與旗標，以逗號分隔。 第一個值在1到100的範圍內，並定義品質。 第二個值可能是0 （代表正常行為），或是1 (代表停用JPEG編碼器通常採用的RGB色度縮減取樣)。

## 默认 {#section-0b25eddd59bc434abfe38eeea9d45df3}

繼承自 `default::JpegQuality` 如果未定義或為空。

## 另请参阅 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
