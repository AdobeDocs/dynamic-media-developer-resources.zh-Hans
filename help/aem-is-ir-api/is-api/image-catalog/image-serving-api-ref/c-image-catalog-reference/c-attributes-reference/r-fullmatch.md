---
description: 目录匹配选项。
solution: Experience Manager
title: 完全匹配
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
TQID: 'https://experienceleague.adobe.com/5eTvORUSVsXHReAaiVMGSizooDQ9Wq--dXrBo0c9C7c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
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
