---
description: 針對縮圖（亦即，如果req=tmb），影像圖層轉換的步驟2會修改如下。
solution: Experience Manager
title: 縮圖縮放
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# 縮圖縮放{#thumbnail-scaling}

針對縮圖（亦即，如果req=tmb），影像圖層轉換的步驟2會修改如下。

* `2.` 若 `size=` 已指定，將（裁切）影像調整到 `size=` 使用縮圖規則重新計算。 若 `size=` 未指定，縮放依據 `res=`，或，如果 `res=` 未指定，請使用下面概述的縮圖規則將（裁切）影像調整到畫布矩形中。
