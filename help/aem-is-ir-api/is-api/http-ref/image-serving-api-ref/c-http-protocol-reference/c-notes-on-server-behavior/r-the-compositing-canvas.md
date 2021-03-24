---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果未显式指定图层0的`size=`，则使用图层变换来计算合成画布的大小（请参阅下面的内容）。

如果`req=tmb`，则合成画布的大小由为图层0指定的`size=`决定，或者，如果未指定大小，则合成画布大小将设置为视图矩形（请参阅下文）。
