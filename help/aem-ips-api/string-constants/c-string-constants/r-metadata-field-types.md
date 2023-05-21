---
description: 由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。
solution: Experience Manager
title: 中繼資料欄位型別
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# 中繼資料欄位型別{#metadata-field-types}

由MetadataField/type、saveMetadataFieldParam/fieldType和createMetadataField/fieldType使用。

语法

## 值 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]：特殊案例 [!DNL `SingleFixedTag`] ，且不可修改的字典初始化為值 [!DNL `True`] 和 [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]：來自關閉字典的零個或多個字串值。 只有管理員使用者可以修改字典。
* [!DNL `MultiTag`]：零個或多個字串值。
* [!DNL `SingleFixedTag`]：來自已關閉字典的單一字串值。 若 `setAssetMetadata` 或 `batchSetAssetMetadata` 以不在字典中的值呼叫，則會傳回錯誤。 只有管理員使用者可以修改字典。

* [!DNL `SingleTag`]：任何單一字串值。
* [!DNL `String`]
