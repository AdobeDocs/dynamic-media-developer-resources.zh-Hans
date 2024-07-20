---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果未显式指定图层0的`size=`，则使用图层转换计算合成画布的大小（请参阅下文）。

如果`req=tmb`，则合成画布的大小由为图层0指定的`size=`确定；如果未指定大小，则合成画布大小将设置为视图矩形（请参阅下文）。
