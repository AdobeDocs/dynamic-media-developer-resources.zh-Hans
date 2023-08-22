---
title: 大小
description: 图层大小。 指定在将旋转=、透视=和延伸=应用于图层之前，图层的大小或最大图层大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# 大小{#size}

图层大小。 指定在将旋转=、透视=和延伸=应用于图层之前，图层的大小或最大图层大小。

` size= *`宽度`*, *`高度`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽度 </span>， <span class="varname"> 高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>以像素（int、int、0或更大）为单位的图层大小限制。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>， <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>相对于0层大小归一化的层大小约束（实际、实际、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

为图像图层指定时，size=将限制图层图像的宽度或/或高度。 图像将缩放为不大于 `size=`. 如果指定了规范化大小，则它是相对于层0的大小的。 如果两者 *`width`* 和 *`height`* 指定，则缩放源图像(在 `crop=` ，这样任何尺寸都不会超过指定的大小。 在所有情况下，源矩形的长宽比都保持不变。 或者 *`width`* 或 *`height`* 可设置为0；在此情况下，该值由服务器根据图像的纵横比计算。

指定文本图层时， `size=` 指定文本框大小。 *`width`* 为必填项； *`height`* 可以设置为0，在这种情况下，使用布局文本的高度作为图层高度。 默认情况下，文本布局引擎会插入换行符，以确保文本始终水平适应可用空间。 如果 *`height`* 指定时，将裁剪不符合可用空间的行( `text=`)或省略( `textPs=`)。 `text=` 支持其他适应模式；请参阅 `textAttr=` 以了解详细信息。

指定纯色图层时， `size=` 定义确切的图层大小；必须同时指定这两个值（除非提供了蒙版）。 如果 `mask=` 还指定了，将调整蒙版图像大小以适应 `size=` 与图像图层中的图像缩放方式相同。

## 属性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

层属性。 应用到图层0，如果 `layer=comp`. `sizeN=` 不允许用于 `layer=0` 或 `layer=comp`. `sizeN=` 允许用于 `layer=0` 和 `layer=comp` 仅在定义水印图像的目录记录中。 在本例中， `sizeN` 定义水印图像相对于将应用水印的复合图像的缩放比例。 如果 `size=` 已指定， `res=` 和 `scale=` 将忽略此图层的。 被效果层忽略。

## 默认 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，则图层大小不受限制。 对于图像图层，然后基于图层图像大小确定图层大小 `crop=`， `scale=`，或 `res=` 已应用操作。 对于文本图层，如果 `size=` 未指定时，将自动调整图层大小以适合渲染的文本。

纯色图层需要完全指定的 `size=`， a `mask=`，或 `clipPath=`.

## 示例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

请参阅 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[缩放=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ， [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)， [蒙版=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
