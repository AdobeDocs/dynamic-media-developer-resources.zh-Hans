---
description: 图层背景颜色。 指定当前图层的背景颜色和不透明度。
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
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

在层的边界矩形内的透明和半不透明区域在应用* `opac=`、`rotate=`和`extend=`之后用指定的颜色*填充。

## 属性 {#section-19dfc13e997f4a33889a1df1e4ad50b9}

层属性。 在`layer=comp`时应用于当前层或应用于层0。 被效果层忽略。

*`color`* 假定存在于对应于像素类型的工作颜色空间中 *`color`*。*`color`* 如果最终层图像具有不同的像素类型，则精确转换。

## 默认 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0（完全透明）。

## 示例 {#section-6e14fcf1d31e432dbdb56b9320904453}

请参阅[color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)。

## 另请参阅 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
