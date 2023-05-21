---
description: 回覆影像大小限制。 可傳回給使用者端的最大回覆影像寬度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# MaxPix{#maxpix}

回覆影像大小限制。 可傳回給使用者端的最大回覆影像寬度和高度。

如果要求會導致回覆影像的寬度或高度大於，則伺服器會傳回錯誤 `attribute::MaxPix`.

## 屬性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

兩個大於0的整數，以逗號分隔。 寬度和高度（畫素）。 也可以設定為 `0,0` 以允許任何回覆影像大小不受限制。

## 默认 {#section-1003537434da432fb2af100ecdbf9d72}

繼承自 `default::MaxPix` 如果未定義或為空。

## 另请参阅 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
