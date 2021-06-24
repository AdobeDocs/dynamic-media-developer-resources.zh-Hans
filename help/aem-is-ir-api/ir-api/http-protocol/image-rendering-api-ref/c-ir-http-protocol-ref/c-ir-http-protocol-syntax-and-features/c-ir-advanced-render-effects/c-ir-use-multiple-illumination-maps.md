---
description: 某些应用可能需要不同种类材料的不同照明图。
solution: Experience Manager
title: 使用多个照明图
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 使用多个照明图{#using-multiple-illumination-maps}

某些应用可能需要不同种类材料的不同照明图。

每个晕影最多可创作三个照明图。 使用`illum=`和或`gloss=`命令选择用于渲染操作的照明图。

**默认** 选择如果 `illum=` 和 `gloss=` 未指定，则渲染器将使用第一个创作的照明图（通常为映射A，即“平面”照明图）。

**自动选择`gloss=`** 如果 `illum=` 未指定或设置为–1，则渲染器将指定值与与晕影中每个照明图 `gloss=` 关联的光泽值进行比较，并选择其光泽值最接近指定值的照明图 `gloss=`。

**显式选择`illum=`** 如果 `illum=` 指定了，并将设置为0、1或2，则渲染器将使用相应的照明图； `gloss=` 将忽略，以便选择照明图。

如果晕影只包含一个照明映射，则渲染器将使用该映射并忽略`illum=`和`gloss=`命令。
