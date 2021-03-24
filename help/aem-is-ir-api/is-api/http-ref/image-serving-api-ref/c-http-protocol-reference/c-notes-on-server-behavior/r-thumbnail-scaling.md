---
description: 对缩览图（即，如果req=tmb）修改了图像图层变换的步骤2。
solution: Experience Manager
title: 缩览图缩放
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 缩览图缩放{#thumbnail-scaling}

对缩览图（即，如果req=tmb）修改了图像图层变换的步骤2。

* `2.` 如果 `size=` 已指定，请使用缩览图规则将（裁剪的）图 `size=` 像调整到矩形中。如果未指定`size=`，则根据`res=`进行缩放，或者，如果未指定`res=`，则使用下面概述的缩略图规则将（裁剪的）图像调整到画布矩形中。

