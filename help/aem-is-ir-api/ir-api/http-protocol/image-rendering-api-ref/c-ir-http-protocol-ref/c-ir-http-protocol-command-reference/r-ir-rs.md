---
description: 高级渲染设置。 指定在渲染当前选定内容时要应用的高级渲染设置。
solution: Experience Manager
title: rs
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# rs{#rs}

高级渲染设置。 指定在渲染当前选定内容时要应用的高级渲染设置。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>呈现设置字符串。 </p></td> 
 </tr> 
</table>

用于微调呈现外观。 使用晕影创作工具(Dynamic Media图像创作包的一部分)的渲染功能创建渲染设置字符串。

## 属性 {#section-9a2b2228789046658cb80eddf343af75}

材料属性。

## 默认 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 示例 {#section-47e4811882574441a4d517e42a35f352}

在图像创作中进行一些实验后，确定USM(USM)可为给定的应用程序和材料提供正确的锐化量。 配置USM的呈现设置字符串将复制到`rs=`命令中以与以下材料一起使用：

`…&rs=U2V20W50X2&…`

## 另请参阅 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
