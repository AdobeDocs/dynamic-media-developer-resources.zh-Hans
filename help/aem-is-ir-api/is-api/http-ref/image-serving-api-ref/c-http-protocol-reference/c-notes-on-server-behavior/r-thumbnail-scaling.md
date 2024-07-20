---
title: 缩略图缩放
description: 对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# 缩略图缩放{#thumbnail-scaling}

对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。

* `2.`如果指定了`size=`，则使用缩略图规则将（裁剪的）图像调整到`size=`矩形。 如果未指定`size=`，则根据`res=`进行缩放；如果未指定`res=`，则使用下面概述的缩略图规则将（裁切）图像调整到画布矩形中。
