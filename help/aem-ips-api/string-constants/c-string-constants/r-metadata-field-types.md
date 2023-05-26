---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 元数据字段类型
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# 元数据字段类型{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]：特殊情况 [!DNL `SingleFixedTag`] 使用初始化为值的不可修改词典 [!DNL `True`] 和 [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]：来自已关闭字典的零个或多个字符串值。 只有管理员用户可以修改字典。
* [!DNL `MultiTag`]：零个或多个字符串值。
* [!DNL `SingleFixedTag`]：来自已关闭词典的单个字符串值。 如果 `setAssetMetadata` 或 `batchSetAssetMetadata` 用不在字典中的值调用，将返回错误。 只有管理员用户可以修改字典。

* [!DNL `SingleTag`]：任意单个字符串值。
* [!DNL `String`]
