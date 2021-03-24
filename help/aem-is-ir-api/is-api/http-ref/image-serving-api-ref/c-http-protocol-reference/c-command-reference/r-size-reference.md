---
description: 图层大小。 指定图层的大小或最大图层大小，然后将rotate=、perspective=和extend=应用于图层。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---


# 大小{#size}

图层大小。 指定图层的大小或最大图层大小，然后将rotate=、perspective=和extend=应用于图层。

` size= *`宽`*, *`高`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽 </span>度， <span class="varname"> 高度  </span> </span> </p> </td> 
  <td class="stentry"> <p>图层大小约束(以像素为单位（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>图层大小约束相对于图层0大小标准化（实、实、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

为图像图层指定时，size=将限制图层图像的宽度或高度，或者同时限制两者。 图像将缩放为不大于`size=`。 如果指定了标准化大小，则它相对于图层0的大小。 如果同时指定了&#x200B;*`width`*&#x200B;和&#x200B;*`height`*，则缩放源图像（在应用`crop=`之后），以使这两个维度均不超过指定的大小。 在所有情况下都保持源矩形的长宽比。 *`width`*&#x200B;或&#x200B;*`height`*&#x200B;可设置为0;在这种情况下，该值由服务器根据图像的长宽比计算。

当为文本图层指定时，`size=`将指定文本框大小。 *`width`* 是必需的； *`height`* 可以设置为0，在这种情况下，布局文本的高度将用作图层高度。默认情况下，文本布局引擎插入换行符以确保文本始终水平适合可用空间。 如果指定&#x200B;*`height`*，则不适合可用空间的行将被剪切(`text=`)或省略(`textPs=`)。 `text=` 支持额外的适合模式；有关详细信息， `textAttr=` 请参阅。

当为纯色图层指定时，`size=`定义确切的图层大小；必须指定这两个值（除非提供蒙版）。 如果还指定了`mask=`，则蒙版图像的大小将与图像图层中图像缩放方式相同，以适合`size=`。

## 属性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

图层属性。 如果`layer=comp`，则应用于层0。 `sizeN=` 不允许 `layer=0` 或 `layer=comp`。`sizeN=` 仅允许在定 `layer=0` 义 `layer=comp` 水印图像的目录记录中使用。在这种情况下，`sizeN`定义水印图像相对于要应用水印的复合图像的缩放。 如果指定`size=`，则忽略此图层的`res=`和`scale=`。 被效果图层忽略。

## 默认 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，则图层大小不受约束。然后，对于图像图层，在应用了任何`crop=`、`scale=`或`res=`操作后，根据图层图像大小确定图层大小。 对于文本图层，如果未指定`size=`，则会自动调整图层大小以适合渲染的文本。

纯色图层需要完全指定的`size=`、`mask=`或`clipPath=`。

## 示例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另请参阅 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,res [=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=mask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)=,  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) [,剪辑路径=,文图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
