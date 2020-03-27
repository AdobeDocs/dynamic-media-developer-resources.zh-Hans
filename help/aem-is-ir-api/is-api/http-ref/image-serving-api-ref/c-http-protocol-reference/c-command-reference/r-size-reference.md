---
description: 图层大小。 指定图层的大小或最大图层大小，然后将rotate=、perspective=和extend=应用于图层。
seo-description: 图层大小。 指定图层的大小或最大图层大小，然后将rotate=、perspective=和extend=应用于图层。
seo-title: 大小
solution: Experience Manager
title: 大小
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 大小{#size}

图层大小。 指定图层的大小或最大图层大小，然后将rotate=、perspective=和extend=应用于图层。

` size= *`宽`*, *`高`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽 </span>度， <span class="varname"> 高 </span> 度 </span> </p> </td> 
  <td class="stentry"> <p>图层大小约束（以像素为单位）（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width N </span>, <span class="varname"> height N </span></span> </p> </td> 
  <td class="stentry"> <p>图层大小约束相对于图层0大小标准化(real、real、0.0...1.0)。 </p> </td> 
 </tr> 
</table>

为图像图层指定时，size=将限制图层图像的宽度或高度，或者同时限制两者。 图像将缩放为不大于 `size=`。 如果指定了标准化大小，则它相对于图层0的大小。 如果同时 *`width`* 指定和 *`height`* 指定了源图像，则缩放（应用后）源图 `crop=` 像，使其尺寸均不超过指定大小。 在所有情况下，都将保持源矩形的长宽比。 或 *`width`* 者 *`height`* 可设置为0;在这种情况下，该值由服务器根据图像的长宽比计算。

为文本图层指定时， `size=` 指定文本框大小。 *`width`* 必填；可 *`height`* 以将其设置为0，在这种情况下，布局文本的高度将用作图层高度。 默认情况下，文本布局引擎插入换行符，以确保文本始终水平适合可用空间。 如 *`height`* 果指定，将剪切()或省略()不适合可用空 `text=`间的 `textPs=`线。 `text=` 支持额外的适应模式；有关详细信息， `textAttr=` 请参阅。

当为纯色图层指定时，会定 `size=` 义确切的图层大小；必须指定这两个值（除非提供遮罩）。 如果 `mask=` 也指定了遮罩图像，则遮罩图像的大小将调整为与在图 `size=` 像图层中缩放图像的方式相同。

## 属性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

图层属性。 如果为，则应用于图层0 `layer=comp`。 `sizeN=` 不允许 `layer=0` 或 `layer=comp`。 `sizeN=` 仅在定义水 `layer=0` 印图 `layer=comp` 像的目录记录中允许。 在这种情况下， `sizeN` 定义水印图像相对于要应用水印的复合图像的缩放比例。 如果 `size=` 指定， `res=` 则 `scale=` 忽略此层。 被效果图层忽略。

## 默认 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，则图层大小不受约束。 对于图像图层，在应用了任何、或操作后，根据图层图像大 `crop=`小确 `scale=`定图 `res=` 层大小。 对于文本图层，如 `size=` 果未指定，图层将自动调整大小以适合渲染的文本。

纯色图层需要完全指定 `size=`、a `mask=`或 `clipPath=`。

## 示例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

请参 [阅模板中](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 的 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)mask= [，剪辑路径](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[=Path=AltoStextLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
