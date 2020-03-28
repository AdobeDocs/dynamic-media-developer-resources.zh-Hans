---
description: 图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。
seo-description: 图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。
seo-title: 锚记
solution: Experience Manager
title: 锚记
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 锚记{#anchor}

图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐标</span></span> </p> </td> 
  <td class="stentry"> <p>源图像左上角的像素偏移量(int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>与源图像中心的归一化偏移（实数、实数） </p></td> 
 </tr> 
</table>

锚点与图像一起转换并成为图层来源点(除非也指定了该点，在这种情况下 `origin=` ，仅用作旋转中心 `anchor=``rotate=`)。

`anchorN=0,0` 将图像锚点放在源图像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位于左上角， `anchorN=0.5,0.5` 位于源图像的右下角。

## 属性 {#section-f08942bc6aae46a8b5d341faaff80640}

源图像属性。 应用于当前层，或应用于层0（如果） `layer=comp`。

## 默认 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果 `anchor=` 未指定，则使用catalog::Anchor。 如果 `catalog::Anchor` 未定义，则使用图像矩形的中心(与指定相同 `anchorN=0,0`)。

涉及文本图层和 `textPs=` 涉及图层的文本图 `clipPath=` 层可能具有不同的默认锚点。

## 示例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

请参阅模板中的“示例C [”](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目录：:::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [来源=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)，旋 [转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [路径=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[，锚点文本层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
