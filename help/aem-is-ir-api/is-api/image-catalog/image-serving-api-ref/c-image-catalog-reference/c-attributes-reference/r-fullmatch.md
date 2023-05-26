---
description: 目录匹配选项。
solution: Experience Manager
title: 完全匹配
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# 完全匹配{#fullmatch}

目录匹配选项。

将目录条目指定为 `*`rootId`*/ *`imageId`*` HTTP请求中的对。 解析时，如果满足以下条件，则选择目录 `*`rootId`*` 匹配 `attribute::RootId` 值，并通过匹配来标识目录记录 `*`imageId`*` 带有 `catalog::Id` 值。 如果找到目录，但没有匹配的目录条目 `*`imageId`*`，则服务器可以执行以下两项操作之一：

如果 `attribute::FullMatch` 未设置，服务器将使用匹配目录的属性。 在这个案例中， `*`rootId`*` 替换为 `attribute::RootPath` (或 `default::RootPath`（如果未在此目录中指定）。

如果 `attribute::FullMatch` 设置，服务器将完全忽略目录（就像没有匹配的目录一样），然后继续使用默认目录属性。 在这个案例中， `*`rootId`*` 保留路径的一部分(在前面加上 `default::RootPath`)。

## 属性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

标记. 设置为0表示默认行为，设置为1表示启用完全匹配行为。

## 默认 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

继承自 `default::FullMatch` 如果未定义或为空。

## 另请参阅 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute：：RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
