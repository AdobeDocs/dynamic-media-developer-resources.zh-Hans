---
title: 对齐
description: 纹理渲染对齐方式。 指定要使用所选晕影对象定义的原点中的哪一个。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---

# 对齐 {#align}

纹理渲染对齐方式。 指定要使用所选晕影对象定义的原点中的哪一个。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>默认（居中对齐）原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>连续匹配来源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>随机对齐。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>用户定义的来源。 </p></td> 
 </tr> 
</table>

渲染器将纹理应用于对象，以便纹理锚点( `anchor=`)与指定的原点重合。

每个对象最多可定义六个原点(0、1、3、4、5、6)。 如果 `align` 指定了value，但晕影对象未定义对应的原点，将使用默认(center-match)原点。

`align=2` 指定随机纹理对齐，在这种情况下 `anchor=` 实际上被忽略了。

主要用于装饰材料，可能用于服装织物，以管理相邻物体之间的纹理对齐。

## 属性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材质属性。 如果选择了壁、机箱、设备或窗口覆盖框架对象，或者材料不是可重复的纹理，则忽略此项。

## 默认 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`，如果材料基于目录条目，则值为0（居中匹配）。

## 另请参阅 {#section-945d1ce275df487d9d564d4043156c79}

[catalog：：Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ， [锚点=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
