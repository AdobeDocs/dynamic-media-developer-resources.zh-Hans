---
title: 缩略图缩放
description: 对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# 缩略图缩放{#thumbnail-scaling}

对于缩略图（即，如果req=tmb），图像图层转换的第2步将修改如下。

* `2.`如果指定了`size=`，则使用缩略图规则将（裁剪的）图像调整到`size=`矩形。 如果未指定`size=`，则根据`res=`进行缩放；如果未指定`res=`，则使用下面概述的缩略图规则将（裁切）图像调整到画布矩形中。
