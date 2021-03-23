---
description: 目录记录标识符
solution: Experience Manager
title: Id
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# Id {#id}

Platform Server查找图像数据文件中记录时使用的索引键值。

通常，如果SKU具有多个图像，则会提供一个简短且唯一的图像标识符，例如SKU编号，并可能带有某种图像后缀。 可能还是一个更复杂的字符串，看起来更像文件路径，支持使用图像服务轻松实现网站的复制。

## 属性 {#id-properties}

文本字符串。 必需. 图像数据表的主索引键。 每个catalog::Id值在表中必须唯一。

## 默认 {#id-default}

无。

## 另请参阅 {#id-seealso}

[属性：:RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)