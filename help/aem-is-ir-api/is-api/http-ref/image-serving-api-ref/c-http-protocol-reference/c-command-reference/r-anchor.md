---
description: 图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。
seo-description: 图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。
seo-title: 锚记
solution: Experience Manager
title: 锚记
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 3%

---


# 锚记{#anchor}

图像锚点。 在应用变换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>源图像左上角的像素偏移(int， int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>从源图像中心标准化的偏移（实、实） </p></td> 
 </tr> 
</table>

锚点随图像一起变换并成为图层来源点（除非也指定了`origin=`，在这种情况下，`anchor=`仅用作`rotate=`的旋转中心）。

`anchorN=0,0` 将图像锚点放在源图像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位于左上角， `anchorN=0.5,0.5` 位于源图像的右下角。

## 属性 {#section-f08942bc6aae46a8b5d341faaff80640}

源图像属性。 应用于当前图层，或应用于`layer=comp`时的图层0。

## 默认 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果未指定`anchor=`，则使用catalog::Anchor。 如果未定义`catalog::Anchor`，则使用图像矩形的中心（与指定`anchorN=0,0`相同）。

涉及`textPs=`的文本图层和涉及`clipPath=`的图层可能具有不同的默认锚点。

## 示例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的“Example C”。

## 另请参阅 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目录：：锚点](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [来源](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)=，旋 [转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [剪](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)辑路径 [=，文图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
