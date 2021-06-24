---
description: 图层大小。 指定在对图层应用rotate=、perspective=和extend=之前图层的大小或最大图层大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---

# 大小{#size}

图层大小。 指定在对图层应用rotate=、perspective=和extend=之前图层的大小或最大图层大小。

` size= *``*, *`widthheight`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽 </span>度，高 <span class="varname"> 度  </span> </span> </p> </td> 
  <td class="stentry"> <p>图层大小约束(以像素为单位（整数、整数、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>层大小约束相对于层0大小进行标准化（实数、实数、0.0..1.0）。 </p> </td> 
 </tr> 
</table>

为图像图层指定时，size=将限制图层图像的宽度或高度，或者同时限制这两者。 图像将缩放为不大于`size=`。 如果指定了标准化大小，则它相对于层0的大小。 如果同时指定了&#x200B;*`width`*&#x200B;和&#x200B;*`height`*，则会缩放源图像（在应用`crop=`之后），以便这两个维度都不超过指定的大小。 在所有情况下，源矩形的宽高比都保持不变。 *`width`*&#x200B;或&#x200B;*`height`*&#x200B;可设置为0;在这种情况下，值由服务器根据图像的宽高比来计算。

为文本层指定后，`size=`会指定文本框大小。 *`width`* 必需； *`height`* 可以设置为0，在这种情况下，将布局文本的高度用作层高度。默认情况下，文本布局引擎会插入换行符，以确保文本始终水平放入可用空间。 如果指定了&#x200B;*`height`*，则不适合可用空间的行将被剪切(`text=`)或忽略(`textPs=`)。 `text=` 支持附加的适配模式；有关详细信息， `textAttr=` 请参阅。

当为实色层指定时，`size=`定义确切的层大小；必须同时指定两个值（除非提供掩码）。 如果还指定了`mask=`，则蒙版图像的大小将与图像层中缩放图像的方式相同，以适合`size=`。

## 属性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

层属性。 如果`layer=comp`，则应用于层0。 `sizeN=` 不允许使用 `layer=0` 或 `layer=comp`。`sizeN=` 仅在定义 `layer=0` 水印 `layer=comp` 图像的目录记录中允许和。在这种情况下，`sizeN`定义水印图像相对于要应用水印的复合图像的缩放比例。 如果指定了`size=`，则此层将忽略`res=`和`scale=`。 被效果层忽略。

## 默认 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，则图层大小不受约束。然后，对于图像层，在应用了任何`crop=`、`scale=`或`res=`操作后，根据层图像大小确定层大小。 对于文本层，如果未指定`size=`，则会自动调整该层的大小以适合呈现的文本。

实色层需要完全指定的`size=`、`mask=`或`clipPath=`。

## 示例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

请参阅[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另请参阅 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
