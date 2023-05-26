---
description: 图像蒙版使用情况。 指定如何使用图像的蒙版或Alpha通道对图像进行操作（例如，colorize=）。 当在效果图层中进行指定时，它允许将效果应用于父图层的背景区域或整个父图层矩形。
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# maskUse{#maskuse}

图像蒙版使用情况。 指定如何使用图像的蒙版或Alpha通道对图像进行操作（例如，colorize=）。 当在效果图层中进行指定时，它允许将效果应用于父图层的背景区域或整个父图层矩形。

`maskUse=norm|invert|off`

下表说明了 `maskUse=` 取决于与图层图像关联的蒙版（alpha通道）的可用性和类型。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 无蒙版</b> </th> 
   <th class="entry"> <b> 未关联的Alpha（或单独的蒙版图像）</b> </th> 
   <th class="entry"> <b> 相关（预乘）Alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 填充了实心黑色的矩形上的图像前景区域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 范数 </span> </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 图像的前景区域 </p> </td> 
   <td> <p> 图像或图层的前景区域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反转 </span> </p> </td> 
   <td> <p> 隐藏图层 </p> </td> 
   <td> <p> 图像的背景区域 </p> </td> 
   <td> <p> 用纯黑色填充的图像或图层的背景区域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f36ad1af348e45aeb3eb336544df30b0}

图像或图层属性。 如果符合以下条件，则应用于图层0 `layer=comp`. 如果在效果层中指定，该命令将修改从父层继承的蒙版。

的行为 `maskUse=` 未定义，当没有适用的图像蒙版时，通过文本或纯色图层指定时，不受支持(通过 `mask=` 或 `catalog::Mask`)。

## 默认 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 示例 {#section-daa371e9be5547368ff6772342acba0a}

为图像的背景区域着色；图像前景由单独的蒙版图像定义。 如果图像未修改，则通过将彩色图像背景叠加到顶部来达到此目的：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另请参阅 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ， [蒙版=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
