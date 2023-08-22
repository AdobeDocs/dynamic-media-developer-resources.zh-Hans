---
title: 来源
description: 图层原点。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# 来源{#origin}

图层原点。

`origin= *`坐标`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐标</span> </p></td> 
  <td class="stentry"> <p>从图层矩形左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从图层矩形中心的规范化偏移（实际、实际）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>层矩形始终包括以下内容的任何修改： `extend=`.

定义图层矩形的对齐点，用于相对于图层0通过定位图层矩形 `pos=`. `originN=0,0` 将图层原点定位在图层矩形的中心。 `originN=-0.5,-0.5` 和 `origin=0,0` 是左上角，并且 `originN=0.5,0.5` 是图层矩形的右下角。

## 属性 {#section-60f639e36ada43d1abc6bfc100afc925}

层属性。 应用到当前图层，或应用到图层0，如果 `layer=comp`. 不受图层转换影响( `crop=`， `scale=`， `rotate=`， `flip=`)应用于图层源。 覆盖 `anchor=`. 被效果层忽略。

## 默认 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果 `origin=` 未指定，图层原点是通过将图层变换应用于图像锚点来确定的。 如果不知道图像锚点，则图层矩形的中心( `originN=0,0`)已使用。

## 示例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

请参阅中的示例A [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
