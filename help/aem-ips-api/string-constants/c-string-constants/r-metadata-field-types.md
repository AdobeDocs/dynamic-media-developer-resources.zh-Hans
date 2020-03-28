---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-title: 元数据字段类型
solution: Experience Manager
title: 元数据字段类型
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# 元数据字段类型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:具有不可修 [!DNL `SingleFixedTag`] 改的字典的特殊情况被初始化为值 [!DNL `True`] 和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:关闭词典中的零个或多个字符串值。 只有管理员用户可以修改词典。
* [!DNL `MultiTag`]:零个或多个字符串值。
* [!DNL `SingleFixedTag`]:封闭词典中的单个字符串值。 如果 `setAssetMetadata` 使用 `batchSetAssetMetadata` 词典中不存在的值调用或调用，则将返回错误。 只有管理员用户可以修改词典。

* [!DNL `SingleTag`]:任何单个字符串值。
* [!DNL `String`]

