---
description: 对于缩略图（即，如果req=tmb），图像图层转换的步骤2将修改如下。
solution: Experience Manager
title: 缩略图缩放
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# 缩略图缩放{#thumbnail-scaling}

对于缩略图（即，如果req=tmb），图像图层转换的步骤2将修改如下。

* `2.` 如果 `size=` 指定，将（裁切的）图像调整到 `size=` 使用缩略图规则进行矩形。 如果 `size=` 未指定，缩放基于 `res=`，或者，如果 `res=` 未指定，请使用下面概述的缩略图规则将（裁切）图像调整到画布矩形中。
