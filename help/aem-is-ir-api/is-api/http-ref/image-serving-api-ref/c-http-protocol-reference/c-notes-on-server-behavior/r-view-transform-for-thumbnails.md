---
description: 回應req=tmb請求傳回給使用者端的影像是透過考量下列值wid=、hei=、屬性DefaultThumbPix和屬性MaxPix從複合影像衍生。
solution: Experience Manager
title: 縮圖的檢視轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 縮圖的檢視轉換{#view-transform-for-thumbnails}

回應req=tmb請求傳回給使用者端的影像是透過考量下列值從複合影像衍生： wid=、hei=、attribute：：DefaultThumbPix和attribute：：MaxPix。

1. **計算檢視矩形**  — 使用 `wid=` 或寬度值 `attribute::DefaultThumbPix` 以取得檢視矩的寬度。 使用 `hei=` 或高度值 `attribute::DefaultThumbPix` 作為高度。 必須在此步驟中完全指定檢視矩形。 (請注意，如果沒有，則檢視矩形與圖層0矩形相同 `size=`指定給圖層0)。
1. **縮放複合** - If `catalog::ThumbType=Crop`，則複合影像會縮放至可能的最小影像，同時仍填滿整個檢視矩形；會裁剪額外的影像資料。 若 `catalog::ThumbType= Fit`，然後複合影像會縮放至可能的最大影像，同時仍然將整個複合影像調整至檢視矩形。 若 `catalog::ThumbType=Texture`，複合完全不會縮放以保留中指定的解析度 `catalog::ThumbRes`.
1. **填色和裁切**  — 檢視矩形中填滿 `bgc=` 顏色(如果未指定，則使用 `attribute::ThumbBkgColor`)。 縮放的複合會使用屬性來對齊檢視矩形： `ThumbHorizAlign` 和屬性： `ThumbVertAlign`. 縮放的複合隨即會與填色檢視矩形合併，而不需進一步縮放。 超出檢視矩形的複合區域會被裁切。
