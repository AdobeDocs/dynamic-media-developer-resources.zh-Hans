---
description: 預設檢視大小。
solution: Experience Manager
title: 預設畫素
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# 預設畫素{#defaultpix}

預設檢視大小。

如果要求未明確使用指定檢視大小，伺服器會將回覆影像限製為不得大於此寬度與高度。 `wid=`， `hei=`，或 `scl=`.

## 屬性 {#section-c3e658cf82c540d986b118f74f0fe1b2}

0或更大的兩個整數，以逗號分隔。 寬度和高度（畫素）。 可將任一或兩個值都設定為0，以保持其不受限制。

不適用於巢狀/內嵌請求。

## 默认 {#section-b7338b2bf5114fff83b0714a57b20639}

繼承自 `default::DefaultPix` 如果未定義或為空。

## 另请参阅 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [catalog：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
