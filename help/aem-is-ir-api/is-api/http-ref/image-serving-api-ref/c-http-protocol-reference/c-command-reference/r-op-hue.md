---
description: 调整色相。 将图层或复合图像的每个可见像素的色相按指定数量移动。
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---


# op_hue{#op-hue}

调整色相。 将图层或复合图像的每个可见像素的色相按指定数量移动。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相调整(-180...+180 int)。 </p></td> 
 </tr> 
</table>

基于360度色相范围。

## 属性 {#section-55779644700b4c808a624cdf5a04447e}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。 在应用操作之前，CMYK图像或图层将转换为RGB。

## 默认 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`，以保持色相不变。
