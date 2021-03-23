---
description: 高级渲染设置。 指定渲染当前选区时要应用的高级渲染设置。
seo-description: 高级渲染设置。 指定渲染当前选区时要应用的高级渲染设置。
seo-title: rs
solution: Experience Manager
title: rs
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---


# rs{#rs}

高级渲染设置。 指定渲染当前选区时要应用的高级渲染设置。

`rs= *`瓦尔`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 瓦尔</span> </p> </td> 
  <td class="stentry"> <p>渲染设置字符串。 </p></td> 
 </tr> 
</table>

用于微调渲染外观。 使用晕影创作工具(Dynamic Media图像创作包的一部分)的渲染功能创建渲染设置字符串。

## 属性 {#section-9a2b2228789046658cb80eddf343af75}

材料属性。

## 默认 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 示例 {#section-47e4811882574441a4d517e42a35f352}

在图像创作方面进行了一些实验后，确定USM为给定的应用程序和材料提供了正确的锐化量。 配置USM的渲染设置字符串将复制到`rs=`命令中，以用于此材料：

`…&rs=U2V20W50X2&…`

## 另请参阅 {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
