---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 元数据字段类型
feature: Dynamic Media Classic，SDK/API，元数据
role: Developer,Administrator
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# 元数据字段类型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:具有不可修 [!DNL `SingleFixedTag`] 改字典的特殊用例，该字典初始化为值 [!DNL `True`] 和 [!DNL `False`]。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:关闭的词典中的零个或多个字符串值。只有管理员用户才能修改字典。
* [!DNL `MultiTag`]:零个或多个字符串值。
* [!DNL `SingleFixedTag`]:封闭词典中的单个字符串值。如果调用的`setAssetMetadata`或`batchSetAssetMetadata`的值不在词典中，则会返回错误。 只有管理员用户才能修改字典。

* [!DNL `SingleTag`]:任意单个字符串值。
* [!DNL `String`]
