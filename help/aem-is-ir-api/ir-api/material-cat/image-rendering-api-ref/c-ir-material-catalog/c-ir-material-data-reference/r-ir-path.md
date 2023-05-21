---
description: 影像檔案路徑。 紋理或貼花影像檔案的相對路徑和名稱。
solution: Experience Manager
title: 路径 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 路径 *{#path}

影像檔案路徑。 紋理或貼花影像檔案的相對路徑和名稱。

伺服器會將此值與 `attribute::RootPath` 以建置實際的影像檔案路徑。 也可以是絕對路徑。

用於指定材質、封包和視窗遮蓋材料的材質影像檔案，以及貼花和牆壁邊框材料的RGB或RGBA影像檔案。 並非所有的機櫃和視窗遮蓋材料都需要單獨的可重複紋理影像。

## 屬性 {#section-8c12ea24f21d4472be677581893e6681}

文字字串。 材質與貼花材質必須使用，機櫃與視窗遮蓋材質則可選用。 如果已指定，則必須是有效的相對或絕對檔案路徑。 純色材質必須為空白。

## 支援的檔案格式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

影像演算支援與Dynamic Media Image Serving相同的來源影像格式。

需要多個不同解析度的影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時表現最佳。 「影像伺服」包含影像轉換器(IC)公用程式，可從任何支援的格式建立PTIFF影像。

如需支援檔案格式的完整清單，請參閱「影像伺服」檔案中的IC公用程式說明。

## 默认 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

无。

## 另请参阅 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[積體電路公用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ， [attribute：：RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)， [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
