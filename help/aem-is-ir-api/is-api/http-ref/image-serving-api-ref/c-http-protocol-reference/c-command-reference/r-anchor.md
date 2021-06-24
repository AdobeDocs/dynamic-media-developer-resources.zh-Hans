---
description: 图像锚点。 在应用转换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。
solution: Experience Manager
title: 锚记
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# 锚记{#anchor}

图像锚点。 在应用转换(crop=、scale=、rotate=、flip=)之前，定义图像、纯色或文本定界框矩形的锚点。 还用作rotate=的旋转中心。

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>源图像左上角的像素偏移(int， int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>与源图像中心的归一化偏移（实、实） </p></td> 
 </tr> 
</table>

该锚点随图像一起转换，并成为层原点（除非还指定了`origin=`，在这种情况下，`anchor=`仅用作`rotate=`的旋转中心）。

`anchorN=0,0` 将图像锚点放置在源图像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位于左上角， `anchorN=0.5,0.5` 并且位于源图像的右下角。

## 属性 {#section-f08942bc6aae46a8b5d341faaff80640}

源图像属性。 应用于当前层，或在`layer=comp`时应用于层0。

## 默认 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果未指定`anchor=`，则使用catalog::Anchor 。 如果未定义`catalog::Anchor`，则使用图像矩形的中心（与指定`anchorN=0,0`相同）。

涉及`textPs=`的文本层和涉及`clipPath=`的层可能具有不同的缺省锚点。

## 示例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的“示例C”。

## 另请参阅 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[目录：：锚点](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) 、 [原点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、 [旋转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、 [剪辑路径=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、 [文本层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
