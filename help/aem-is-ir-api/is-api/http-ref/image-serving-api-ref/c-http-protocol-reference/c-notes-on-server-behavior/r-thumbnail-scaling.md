---
description: 图像层转换的步骤2被修改如下，用于缩略图（即，如果req=tmb）。
solution: Experience Manager
title: 缩略图缩放
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 缩略图缩放{#thumbnail-scaling}

图像层转换的步骤2被修改如下，用于缩略图（即，如果req=tmb）。

* `2.` 如果 `size=` 已指定，请使用缩略图规则将（裁剪的）图 `size=` 像调整为正文。如果未指定`size=`，则根据`res=`缩放；或者，如果未指定`res=`，则使用下面概述的缩略图规则将（裁剪的）图像调整到画布的正面中。
