---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-title: 合成画布
solution: Experience Manager
title: 合成画布
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果未明确指定图层0的`size=`，则使用图层变换计算合成画布的大小（请参见下文）。

如果`req=tmb`，则复合画布的大小由为图层0指定的`size=`决定；如果未指定大小，则复合画布的大小将设置为视图矩形（请参见下文）。
