---
description: 图像蒙版的使用。 指定图像的蒙版或Alpha渠道用于图像操作的方式（例如，colorize=）。 当在效果图层中指定时，它允许将效果应用于父图层的背景区域或整个父图层矩形。
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# maskUse{#maskuse}

图像蒙版的使用。 指定图像的蒙版或Alpha渠道用于图像操作的方式（例如，colorize=）。 当在效果图层中指定时，它允许将效果应用于父图层的背景区域或整个父图层矩形。

`maskUse=norm|invert|off`

下表说明了`maskUse=`的效果，具体取决于与图层图像关联的蒙版(Alpha渠道)的可用性和类型。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 无蒙版</b> </th> 
   <th class="entry"> <b> 未关联的Alpha（或分离蒙版图像）</b> </th> 
   <th class="entry"> <b> 关联（预乘）alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 用纯黑填充的矩形上的图像前景区域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 规范  </span> </p> </td> 
   <td> <p> 不透明图像矩形 </p> </td> 
   <td> <p> 图像的前景区域 </p> </td> 
   <td> <p> 图像或图层的前景区域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反  </span> </p> </td> 
   <td> <p> 隐藏图层 </p> </td> 
   <td> <p> 图像的背景区域 </p> </td> 
   <td> <p> 用纯黑填充的图像或图层的背景区域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f36ad1af348e45aeb3eb336544df30b0}

图像或图层属性。 如果`layer=comp`，则应用于层0。 如果在效果图层中指定，则命令将修改从父图层继承的蒙版。

当没有适用的图像蒙版时（使用`mask=`或`catalog::Mask`指定），如果使用文本或纯色图层指定，则`maskUse=`的行为是未定义的且不支持的。

## 默认 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 示例 {#section-daa371e9be5547368ff6772342acba0a}

为图像的背景区域着色；图像前景由单独的蒙版图像定义。 如果未修改的图像，则通过将着色图像背景分层到上面即可实现：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另请参阅 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
