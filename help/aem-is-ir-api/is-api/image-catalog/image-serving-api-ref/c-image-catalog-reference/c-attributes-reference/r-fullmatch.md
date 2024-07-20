---
description: 目录匹配选项。
solution: Experience Manager
title: 完全匹配
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# 完全匹配{#fullmatch}

目录匹配选项。

在HTTP请求中将目录条目指定为`*`rootId`*/ *`imageId`*`对。 解析时，如果`*`rootId`*`与目录的`attribute::RootId`值匹配，并且目录记录通过将`*`imageId`*`与`catalog::Id`值匹配来标识，则选择目录。 如果找到目录，但没有与`*`imageId`*`匹配的目录条目，则服务器可以执行以下两项操作之一：

如果未设置`attribute::FullMatch`，服务器将使用匹配目录的属性。 在这种情况下，`*`rootId`*`将替换为`attribute::RootPath`（或者`default::RootPath`，如果未在此目录中指定）。

如果设置了`attribute::FullMatch`，服务器将完全忽略该目录（就像没有匹配的目录一样），并继续使用默认目录属性。 在这种情况下，`*`rootId`*`仍然是路径的一部分（在前`default::RootPath`）。

## 属性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

标志。 设置为0表示默认行为，设置为1表示启用完全匹配行为。

## 默认 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定义或为空，则从`default::FullMatch`继承。

## 另请参阅 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute：：RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
