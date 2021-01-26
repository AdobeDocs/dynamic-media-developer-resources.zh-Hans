---
description: 目录匹配选项。
seo-description: 目录匹配选项。
seo-title: 完全匹配
solution: Experience Manager
title: 完全匹配
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# FullMatch{#fullmatch}

目录匹配选项。

在HTTP请求中，目录条目指定为`*`rootId`*/ *`imageId`*`对。 解析时，如果`*`rootId`*`与目录的`attribute::RootId`值匹配，则选择目录，并通过将`*`imageId`*`与`catalog::Id`值匹配来标识目录记录。 如果找到目录，但没有与`*`imageId`*`匹配的目录条目，则服务器可以执行以下两项操作之一：

如果未设置`attribute::FullMatch`，则服务器将使用匹配目录的属性。 在这种情况下，`*`rootId`*`将替换为`attribute::RootPath`（如果未在此目录中指定，则为`default::RootPath`）。

如果`attribute::FullMatch`已设置，则服务器将完全忽略目录（如果未匹配目录），然后使用默认目录属性继续。 在这种情况下，`*`rootId`*`仍保留路径的一部分（该路径由`default::RootPath`作为前缀）。

## 属性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

标记. 对于默认行为，设置为0或设置为1以启用完全匹配行为。

## 默认 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定义或为空，则从`default::FullMatch`继承。

## 另请参阅 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
