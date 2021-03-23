---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
seo-title: 元数据字段类型
solution: Experience Manager
title: 元数据字段类型
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 1%

---


# 元数据字段类型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:具有不可修 [!DNL `SingleFixedTag`] 改的字典的特例，初始化为值 [!DNL `True`] 和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:关闭词典中的零个或多个字符串值。只有管理员用户可以修改词典。
* [!DNL `MultiTag`]:零个或多个字符串值。
* [!DNL `SingleFixedTag`]:封闭词典中的单个字符串值。如果调用`setAssetMetadata`或`batchSetAssetMetadata`时的值不在词典中，则将返回错误。 只有管理员用户可以修改词典。

* [!DNL `SingleTag`]:任何单个字符串值。
* [!DNL `String`]

