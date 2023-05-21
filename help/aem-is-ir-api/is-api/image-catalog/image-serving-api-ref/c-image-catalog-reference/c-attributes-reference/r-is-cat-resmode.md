---
title: 解析模式
description: 預設重新取樣模式。 指定用來縮放影像資料的預設重新取樣與內插屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# 解析模式{#resmode}

預設重新取樣模式。 指定用來縮放影像資料的預設重新取樣與內插屬性。

使用時機 `resMode=` 請求中未指定。

## 屬性 {#section-493f900be522486f97710cebdc4460c2}

列舉。 設為2 `bilin`， 3表示 `bicub`，或4個 `sharp2` 內插模式(請參閱 [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) 以取得詳細資訊)。 `sharp` (1)已過時。 使用 `sharp2` (4)而非，以獲得最佳結果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

繼承自 `default::ResMode` 如果未定義或為空。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
