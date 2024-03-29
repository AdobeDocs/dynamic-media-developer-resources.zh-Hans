---
title: 锚记
description: 图像锚点。 定义在应用转换(crop=、scale=、rotate=、flip=)之前，图像、纯色或文本边框矩形的锚点。 也用作rotate=的旋转中心。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 锚记{#anchor}

图像锚点。 定义在应用转换(crop=、scale=、rotate=、flip=)之前，图像、纯色或文本边框矩形的锚点。 也用作rotate=的旋转中心。

`anchor= *`坐标`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐标</span> </span> </p> </td> 
  <td class="stentry"> <p>距源图像左上角的像素偏移(int， int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>距源图像中心的规范化偏移（实数、实数） </p></td> 
 </tr> 
</table>

锚点将随图像一起转换，并成为图层原点(除非 `origin=` 指定了，在这种情况下 `anchor=` 仅用作旋转中心 `rotate=`)。

`anchorN=0,0` 将图像锚点放置在源图像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 位于左上角，并且 `anchorN=0.5,0.5` 位于源图像的右下角。

## 属性 {#section-f08942bc6aae46a8b5d341faaff80640}

源图像属性。 应用到当前图层，或应用到图层0，如果 `layer=comp`.

## 默认 {#section-35d369fab1254f1a9b91684a6e169ad1}

如果 `anchor=` 未指定，使用catalog：：Anchor。 如果 `catalog::Anchor` 未定义，则使用图像矩形的中心(与指定 `anchorN=0,0`)。

涉及以下内容的文本图层 `textPs=` 和涉及以下内容的层 `clipPath=` 可能具有不同的默认锚点。

## 示例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

请参阅中的“示例C” [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog：：锚点](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ， [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)， [旋转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
