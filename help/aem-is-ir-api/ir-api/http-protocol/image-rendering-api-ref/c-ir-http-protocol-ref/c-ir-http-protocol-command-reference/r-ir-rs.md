---
title: rs
description: 高级渲染设置。 指定渲染当前选定内容时要应用的高级渲染设置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# rs{#rs}

高级渲染设置。 指定渲染当前选定内容时要应用的高级渲染设置。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>渲染设置字符串。 </p></td> 
 </tr> 
</table>

用于微调渲染外观。 要创建渲染设置字符串，请使用晕影创作工具的渲染功能(Dynamic Media图像创作包的一部分)。

## 属性 {#section-9a2b2228789046658cb80eddf343af75}

材质属性。

## 默认 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 示例 {#section-47e4811882574441a4d517e42a35f352}

在图像创作方面进行了一些实验之后，确定了USM为给定的应用和材料提供了正确的锐化量。 配置USM的渲染设置字符串将会复制到 `rs=` 要与此材料一起使用的命令：

`…&rs=U2V20W50X2&…`

## 另请参阅 {#section-930116e735024a008c994547ba36ee40}

[catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
