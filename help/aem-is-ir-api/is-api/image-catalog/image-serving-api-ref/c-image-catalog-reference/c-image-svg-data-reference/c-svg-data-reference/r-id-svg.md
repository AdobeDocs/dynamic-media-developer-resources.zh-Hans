---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 4%

---

# Id{#id}

通常是簡短且唯一的識別碼（例如SKU編號），可能帶有某種尾碼，例如SKU具有多個影像或地區設定特有的變數。 也可能是更複雜的字串，看起來更像檔案路徑，以支援透過影像伺服輕鬆更新網站。

>[!NOTE]
>
>載入影像目錄時，影像和SVG表格會合併到單一表格中。 兩個表格中的ID值必須是唯一的。 如果影像表格包含具有相同ID值的記錄，則會捨棄SVG記錄。 靜態內容是由個別的表格管理；因此，靜態內容專案和影像/SVG專案可能具有相同的ID值。

## 屬性 {#section-874a6853f67b4b229341ca76682884ae}

文字字串。 必需. 影像/SVG或靜態內容資料表的記錄識別碼。 每個 `catalog::Id` 此影像目錄/SVG目錄或此靜態內容目錄中的值必須是唯一的，且不得包含「，」字元。

## 默认 {#section-a26e7d83a5ee44b5918baef82ee48e14}

无。

## 另请参阅 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute：：RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
