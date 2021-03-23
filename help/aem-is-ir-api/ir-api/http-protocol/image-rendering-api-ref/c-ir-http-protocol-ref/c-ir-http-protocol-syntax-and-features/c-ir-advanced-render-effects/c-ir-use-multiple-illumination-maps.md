---
description: 某些应用可能需要针对不同种类的材料制作不同的照明图。
seo-description: 某些应用可能需要针对不同种类的材料制作不同的照明图。
seo-title: 使用多个照明图
solution: Experience Manager
title: 使用多个照明图
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 使用多个照明映射{#using-multiple-illumination-maps}

某些应用可能需要针对不同种类的材料制作不同的照明图。

可为每个晕影创作最多三个照明图。 使用`illum=`和或`gloss=`命令选择用于渲染操作的照明映射。

**默认** 选择如 `illum=` 果 `gloss=` 既未指定，也未指定，则呈示器将使用第一个创作的照明映射（通常为映射A，即“平面”照明映射）。

**自动选择`gloss=`** 如果 `illum=` 未指定或设置为–1，则渲染器将指定值与晕影中与每个照明 `gloss=` 图关联的光泽值进行比较，并选择其光泽值最接近指定值的照明图 `gloss=`。

**显式选择`illum=`** 如 `illum=` 果指定并设置为0、1或2，则渲染器将使用相应的照明图； `gloss=` 为了选择照明图而忽略。

如果晕影只包含一个照明映射，则渲染器将使用该映射并忽略`illum=`和`gloss=`命令。
