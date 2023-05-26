---
description: 调整色相。 将图层或复合图像的每个可见像素的色相偏移指定的量。
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# op_hue{#op-hue}

调整色相。 将图层或复合图像的每个可见像素的色相偏移指定的量。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相调整，以度为单位(-180...+180 int)。 </p></td> 
 </tr> 
</table>

基于360度的色相范围。

## 属性 {#section-55779644700b4c808a624cdf5a04447e}

“图层”命令。 应用于当前图层或复合图像，如果 `layer=comp`. 被效果层忽略。 在应用操作之前，CMYK图像或图层会转换为RGB。

## 默认 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，表示色相没有变化。
