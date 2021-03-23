---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
seo-title: 合成画布
solution: Experience Manager
title: 合成画布
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果未显式指定图层0的`size=`，则使用图层变换来计算合成画布的大小（请参阅下面的内容）。

如果`req=tmb`，则合成画布的大小由为图层0指定的`size=`决定，或者，如果未指定大小，则合成画布大小将设置为视图矩形（请参阅下文）。
