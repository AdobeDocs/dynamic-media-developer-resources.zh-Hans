---
description: 請注意這些縮圖規則。
solution: Experience Manager
title: 縮圖規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 縮圖規則{#thumbnail-rules}

請注意這些縮圖規則。

1. 若 `catalog::ThumbType=Crop`，然後會將（裁切）影像縮放至可能的最小尺寸，同時仍覆蓋整個目標矩形。 若 `catalog::ThumbType=Fit`，然後會將（裁切）影像縮放至可能的最大尺寸，同時仍讓整個影像符合目標矩形。 若 `catalog::ThumbType=Texture`，則（裁切的）影像會縮放成以下比例： `catalog::ThumbRes` 至 `catalog::Resolution`.
1. 將縮放的影像對齊目標矩形，依據 `attribute::ThumbHorizAlign` 和 `attribute::ThumbVertAlign`.
1. 裁切結果至目標矩形。
