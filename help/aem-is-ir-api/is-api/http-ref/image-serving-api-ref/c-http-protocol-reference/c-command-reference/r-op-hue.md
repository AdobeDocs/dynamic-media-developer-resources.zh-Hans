---
title: op_hue
description: 调整图像色相。 将图层或复合图像的每个可见像素的色相偏移指定的量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
TQID: 'https://experienceleague.adobe.com/6VSkHDcXsf531qB6okDvLt-xIyFoiw-fG3Z11a-Ne5g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 1%

---

# op_hue{#op-hue}

调整图像色相。 将图层或复合图像的每个可见像素的色相偏移指定的量。

`op_hue= *`调整`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">调整</span> </p> </td> 
  <td class="stentry"> <p>色相调整，以度为单位(-180...+180int)。 </p></td> 
 </tr> 
</table>

基于360度的色相范围。

## 属性 {#section-55779644700b4c808a624cdf5a04447e}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。 在应用操作之前，CMYK图像或图层将转换为RGB。

## 默认 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，表示色相没有变化。
