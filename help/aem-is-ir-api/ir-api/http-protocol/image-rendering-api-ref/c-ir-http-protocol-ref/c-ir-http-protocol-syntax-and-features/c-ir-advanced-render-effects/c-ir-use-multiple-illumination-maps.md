---
title: 使用多个照明图
description: 某些应用可能需要不同种类材料的不同照明图。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 使用多个照明图{#using-multiple-illumination-maps}

某些应用可能需要不同种类材料的不同照明图。

每个晕影最多可创作三个照明图。 选择用于渲染操作的照明图，其中 `illum=` 和 `gloss=` 中。

**默认选择**  — 如果 `illum=` 或 `gloss=` 未指定，则渲染器使用第一个创作的照明图（通常为映射A，即“平面”照明图）。

**自动选择`gloss=`**  — 如果 `illum=` 未指定或设置为 `-1`，则渲染器会比较指定的 `gloss=` 值与晕影中每个照明图关联的光泽值。 它会选择其光泽值最接近指定的照明图 `gloss=`.

**显式选择`illum=`**  — 如果 `illum=` 已指定并设置为 `0`, `1`或 `2`，则渲染器使用相应的照明图； `gloss=` 在选择照明图时将被忽略。

如果晕影只包含一个照明图，则渲染器会使用该图并忽略 `illum=` 和 `gloss=` 中。
