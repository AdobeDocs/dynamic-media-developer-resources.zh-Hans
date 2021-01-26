---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-title: 元数据字段类型
solution: Experience Manager
title: 元数据字段类型
topic: Dynamic Media Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 元数据字段类型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:具有不可修 [!DNL `SingleFixedTag`] 改的字典的特例，该字典初始化为值 [!DNL `True`] 和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:关闭的字典中的零个或多个字符串值。只有管理员用户才能修改字典。
* [!DNL `MultiTag`]:零个或多个字符串值。
* [!DNL `SingleFixedTag`]:封闭字典中的单个字符串值。如果调用`setAssetMetadata`或`batchSetAssetMetadata`时的值不在字典中，则将返回错误。 只有管理员用户才能修改字典。

* [!DNL `SingleTag`]:任何单个字符串值。
* [!DNL `String`]

