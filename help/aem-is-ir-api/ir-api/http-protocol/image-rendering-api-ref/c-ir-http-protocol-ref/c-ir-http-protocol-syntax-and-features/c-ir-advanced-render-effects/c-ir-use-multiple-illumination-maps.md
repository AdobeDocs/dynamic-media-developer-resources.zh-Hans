---
title: 使用多个照明地图
description: 某些应用可能要求针对不同材料使用不同的照明地图。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 使用多个照明地图{#using-multiple-illumination-maps}

某些应用可能要求针对不同材料使用不同的照明地图。

可以为每个晕影创作多达三个光照图。 用于渲染操作的照明地图通过 `illum=` 和/或 `gloss=` 命令。

**默认选择** - If `illum=` 或 `gloss=` 如果未指定，则渲染器使用第一个创作的照明地图（通常为地图A，也称为“平坦”照明地图）。

**自动选择`gloss=`** - If `illum=` 未指定或设置为 `-1`，渲染器会比较指定的 `gloss=` 值与晕影中每个照明地图关联的光泽值。 它选择光泽值最接近指定值的光照图 `gloss=`.

**显式选择`illum=`** - If `illum=` 指定并设置为 `0`， `1`，或 `2`，渲染器使用相应的光照图； `gloss=` 在选取照明地图时忽略。

如果晕影仅包含一个照明映射，则渲染器会使用该映射并忽略 `illum=` 和 `gloss=` 命令。
