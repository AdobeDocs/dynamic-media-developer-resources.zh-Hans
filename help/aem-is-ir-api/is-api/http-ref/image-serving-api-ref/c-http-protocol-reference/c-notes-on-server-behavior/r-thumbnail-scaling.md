---
description: 对缩览图（即，如果req=tmb）修改图像图层变换的步骤2。
seo-description: 对缩览图（即，如果req=tmb）修改图像图层变换的步骤2。
seo-title: 缩览图缩放
solution: Experience Manager
title: 缩览图缩放
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# 缩览图缩放{#thumbnail-scaling}

对缩览图（即，如果req=tmb）修改图像图层变换的步骤2。

* `2.` 如果 `size=` 已指定，请使用缩览图规则使（裁剪的）图 `size=` 像适合矩形。如果未指定`size=`，则根据`res=`进行缩放，或者，如果未指定`res=`，则使用下面概述的缩略图规则将（裁剪的）图像调整到画布矩形中。

