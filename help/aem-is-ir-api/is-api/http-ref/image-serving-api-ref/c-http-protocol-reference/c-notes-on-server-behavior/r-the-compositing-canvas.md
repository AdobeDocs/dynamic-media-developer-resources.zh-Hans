---
description: 如果req=img，合成畫布的大小完全由圖層0的大小決定。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

如果req=img，合成畫布的大小完全由圖層0的大小決定。

如果 `size=` 若未明確指定圖層0，則會使用圖層轉換來計算合成畫布的大小（請參閱下文）。

若 `req=tmb`，合成畫布的大小由決定 `size=` 指定圖層0，如果未指定大小，則複合畫布大小會設定為檢視矩形（請參閱下文）。
