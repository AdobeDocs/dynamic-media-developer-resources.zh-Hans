---
description: 纹理渲染对齐方式。 指定将使用所选晕影对象定义的原点。
solution: Experience Manager
title: 对齐
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---

# 对齐{#align}

纹理渲染对齐方式。 指定将使用所选晕影对象定义的原点。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>默认（中心匹配）原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>连续匹配源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>随机对齐。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>用户定义的源。 </p></td> 
 </tr> 
</table>

渲染器将纹理应用于对象，以便纹理锚点(`anchor=`)与指定的原点一致。

每个对象最多可定义6个原点(0、1、3、4、5、6)。 如果指定了`align`值，但晕影对象未定义相应的原点，则使用默认（中心匹配）原点。

`align=2` 指定随机纹理对齐方式，在这种情况下， `anchor=` 会被有效忽略。

主要用于装饰材料，可能是服装面料，以管理相邻物体之间质地的对齐。

## 属性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材料属性。 如果选择了壁、机柜、装置或窗口覆盖框架对象，或者材料不是可重复的纹理，则忽略。

## 默认 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`，如果材料基于目录条目，则为0（中间匹配）。

## 另请参阅 {#section-945d1ce275df487d9d564d4043156c79}

[目录：:Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
