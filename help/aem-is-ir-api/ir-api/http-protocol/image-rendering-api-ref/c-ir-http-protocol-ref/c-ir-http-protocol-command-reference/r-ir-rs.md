---
description: 高级渲染设置。 指定渲染当前选择时要应用的高级渲染设置。
seo-description: 高级渲染设置。 指定渲染当前选择时要应用的高级渲染设置。
seo-title: rs
solution: Experience Manager
title: rs
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# rs{#rs}

高级渲染设置。 指定渲染当前选择时要应用的高级渲染设置。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>渲染设置字符串。 </p></td> 
 </tr> 
</table>

用于微调渲染外观。 使用晕影创作工具(Dynamic Media图像创作包的一部分)的渲染功能创建渲染设置字符串。

## 属性 {#section-9a2b2228789046658cb80eddf343af75}

材料属性。

## 默认 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 示例 {#section-47e4811882574441a4d517e42a35f352}

在进行图像创作方面的一些试验后，确定USM为给定的应用程序和材料提供了正确的锐化量。 配置USM的渲染设置字符串被复制到`rs=`命令中以与此材料一起使用：

`…&rs=U2V20W50X2&…`

## 另请参阅 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
