---
description: 如果req=img，则复合画布的大小完全由图层0的大小决定。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# 合成画布{#the-compositing-canvas}

如果req=img，则复合画布的大小完全由图层0的大小决定。

如果 `size=` 对于未明确指定图层0，将使用图层转换计算合成画布的大小（见下文）。

如果 `req=tmb`，合成画布的大小由 `size=` 为图层0指定，如果未指定大小，则复合画布大小将设置为视图矩形（见下文）。
