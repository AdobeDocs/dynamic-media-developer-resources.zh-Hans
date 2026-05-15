---
title: 使用多个照明地图
description: 有些应用对于不同的材料可能需要不同的照明地图。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
TQID: 'https://experienceleague.adobe.com/VVZ1IdVJ85V-mIrdN6O8Vs-gb4PTsnjxyHnC8oEh1y0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# 使用多个照明地图{#using-multiple-illumination-maps}

有些应用对于不同的材料可能需要不同的照明地图。

可以为每个晕影创作多达三个照明地图。 使用`illum=`和/或`gloss=`命令选择渲染操作的照明映射。

**默认选择** — 如果未指定`illum=`或`gloss=`，渲染器将使用第一个创作的照明映射（通常为映射A，亦即“平坦”照明映射）。

**使用`gloss=`**&#x200B;的自动选择 — 如果未指定`illum=`或将其设置为`-1`，渲染器会将指定的`gloss=`值与晕影中每个照明映射关联的光泽值进行比较。 它选择其光泽值最接近指定`gloss=`的照明映射。

**使用`illum=`**&#x200B;的显式选择 — 如果指定了`illum=`并设置为`0`、`1`或`2`，则渲染器使用相应的照明映射；在选择照明映射时忽略`gloss=`。

如果晕影仅包含一个照明映射，则渲染器使用该映射并忽略`illum=`和`gloss=`命令。
