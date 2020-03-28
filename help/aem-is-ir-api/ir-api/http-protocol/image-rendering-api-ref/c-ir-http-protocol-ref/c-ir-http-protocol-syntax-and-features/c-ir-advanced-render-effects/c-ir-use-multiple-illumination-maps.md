---
description: 某些应用可能需要针对不同种类的材料制作不同的照明图。
seo-description: 某些应用可能需要针对不同种类的材料制作不同的照明图。
seo-title: 使用多个照明图
solution: Experience Manager
title: 使用多个照明图
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用多个照明图{#using-multiple-illumination-maps}

某些应用可能需要针对不同种类的材料制作不同的照明图。

可为每个暗角创作最多三个照明图。 使用和或命令选择用于渲染操作的照 `illum=` 明映 `gloss=` 射。

**默认选择** 如果既未指定 `illum=` ，也未 `gloss=` 指定，则渲染器将使用第一个创作的照明映射（通常为映射A，也称为“平面”照明映射）。

**如果未指定或`gloss=`**设`illum=`置为-1，则渲染器将指定值与暗角中与每个照明映射相关联的光泽值进行比较，并选择其光泽值最接近指定值的照明映射`gloss=``gloss=`。

**明确选择`illum=`**如`illum=`果指定为0、1或2，则渲染器将使用相应的照明图；为`gloss=`了选择照明图而忽略。

如果暗角仅包含一个照明映射，则渲染器将使用该映射并忽略 `illum=` 和命 `gloss=` 令。
