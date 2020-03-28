---
description: 目录匹配选项。
seo-description: 目录匹配选项。
seo-title: 完全匹配
solution: Experience Manager
title: 完全匹配
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 完全匹配{#fullmatch}

目录匹配选项。

在HTTP请求中，目录条目指 ` *``*/ *`定为rootIdimageId`*` 对。 解析时，如果 ` *`rootId与目录值匹配`*` ，则选择目录，并通过将imageId与值匹配来 `attribute::RootId` 标识目录记 ` *``*``catalog::Id` 录。 如果找到目录，但没有与imageId匹配的目录条 ` *`目`*`，则服务器可以执行以下两项操作之一：

如果 `attribute::FullMatch` 未设置，则服务器将使用匹配目录的属性。 在这种情况下， ` *`rootId将替`*` 换为 `attribute::RootPath` ( `default::RootPath`或，如果未在此目录中指定)。

如果 `attribute::FullMatch` 设置了此选项，则服务器将完全忽略目录（就像没有匹配目录一样），并使用默认的目录属性继续操作。 在这种情况下， ` *`rootId`*` 仍保留路径的一部分(前缀为 `default::RootPath`)。

## 属性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

标记. 对于默认行为，设置为0，或设置为1以启用完全匹配行为。

## 默认 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定义 `default::FullMatch` 或为空，则从中继承。

## 另请参阅 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute:::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
