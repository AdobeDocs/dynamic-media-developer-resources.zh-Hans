---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-title: 合成画布
solution: Experience Manager
title: 合成画布
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果 `size=` 未明确指定图层0，则使用图层变换计算合成画布的大小（请参阅下文）。

如 `req=tmb``size=` 果，合成画布的大小由为图层0指定的大小决定，或者，如果未指定大小，则合成画布的大小将设置为视图矩形（请参阅下文）。
