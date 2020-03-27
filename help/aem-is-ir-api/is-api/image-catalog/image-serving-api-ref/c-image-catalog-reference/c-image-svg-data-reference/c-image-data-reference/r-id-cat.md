---
description: 目录记录标识符
solution: Experience Manager
title: Id
topic: Scene7 Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# Id {#id}

索引键值，通过该索引键值，平台服务器将查找图像数据文件中的记录。

通常，如果SKU有多个图像，则短且唯一的图像标识符（如SKU编号）可能带有某种类型的图像后缀。 也可能是一个更复杂的字符串，它看起来更像文件路径，支持使用图像服务轻松地对网站进行追溯。

## 属性 {#id-properties}

文本字符串。 必需. 图像数据表的主索引键。 每个目录：:Id值在表中必须是唯一的。

## 默认 {#id-default}

无。

## 另请参阅 {#id-seealso}

[属性：:RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)