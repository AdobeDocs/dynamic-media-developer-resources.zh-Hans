---
title: 缩略图缩放
description: 对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 缩略图缩放{#thumbnail-scaling}

对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。

* `2.` 如果 `size=` 指定，将（裁剪的）图像调整到 `size=` 使用缩略图规则重新计算。 如果 `size=` 未指定，缩放基于 `res=`，或者，如果 `res=` 未指定，请使用下面列出的缩略图规则将（裁剪的）图像调整到画布矩形中。
