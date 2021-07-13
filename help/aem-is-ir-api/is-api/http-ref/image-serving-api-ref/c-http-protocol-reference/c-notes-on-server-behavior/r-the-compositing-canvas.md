---
description: 如果req=img，则复合画布的大小完全由层0的大小确定。
solution: Experience Manager
title: 复合画布
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# 复合画布{#the-compositing-canvas}

如果req=img，则复合画布的大小完全由层0的大小确定。

如果未明确指定图层0的`size=` ，则使用图层转换来计算复合画布的大小（请参阅下文）。

如果为`req=tmb`，则复合画布的大小由为层0指定的`size=`决定，或者，如果未指定大小，则复合画布的大小将设置为视图矩形（请参阅下文）。
