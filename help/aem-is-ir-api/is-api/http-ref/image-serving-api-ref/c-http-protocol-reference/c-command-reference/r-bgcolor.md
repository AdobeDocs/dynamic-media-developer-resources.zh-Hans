---
description: 图层背景颜色。 指定当前图层的背景颜色和不透明度。
seo-description: 图层背景颜色。 指定当前图层的背景颜色和不透明度。
seo-title: bgColor
solution: Experience Manager
title: bgColor
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%

---


# bgColor{#bgcolor}

图层背景颜色。 指定当前图层的背景颜色和不透明度。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 颜色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，带或不带Alpha。 </p></td> 
 </tr> 
</table>

在应用* `opac=`、`rotate=`和`extend=`之后，图层边界矩形内的透明和半不透明区域将填充指定颜色*。

## 属性 {#section-19dfc13e997f4a33889a1df1e4ad50b9}

图层属性。 应用于当前图层，或应用于`layer=comp`时的图层0。 被效果图层忽略。

*`color`* 假定存在于对应于像素类型的工作颜色空间中 *`color`*。*`color`* 如果最终图层图像具有不同的像素类型，则精确转换。

## 默认 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0（完全透明）。

## 示例 {#section-6e14fcf1d31e432dbdb56b9320904453}

请参阅[color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)。

## 另请参阅 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)blendMode=,  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172), opac [,扩](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [展=,  , Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
