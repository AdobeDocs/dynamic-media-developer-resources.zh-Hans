---
description: Postfix要求修飾元字串。 沒有或多個以「&」字元分隔的「影像伺服」命令。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Postfix要求修飾元字串。 沒有或多個以「&amp;」字元分隔的「影像伺服」命令。

此欄位中的命令一律會覆寫HTTP請求和中的命令 `catalog::Modifier`.

`catalog::PostModifier` 如果某些影像需要特殊設定，而這些設定通常由URL控制，例如 `qlt=` 或 `resmode=`. `catalog::Modifier` 應該用於設定影像目錄中的大多數IS命令。

中允許巨集 `catalog::PostModifier`，只要它們是在相同目錄或預設目錄中定義。 您也可以使用自訂變數。

>[!NOTE]
>
>如果請求涉及多個圖層，則僅請求 `catalog::PostModifier` 套用圖層0。 `catalog::PostModifier` 會忽略其他所有圖層。

## 屬性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文字字串。 可选.

## 默认 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

无。

## 另请参阅 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
