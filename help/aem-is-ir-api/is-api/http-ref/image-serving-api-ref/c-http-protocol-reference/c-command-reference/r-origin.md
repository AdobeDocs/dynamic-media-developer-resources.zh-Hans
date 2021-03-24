---
description: 图层来源。
solution: Experience Manager
title: 来源
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# 来源{#origin}

图层来源。

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>图层矩形左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>与图层矩形中心的标准化偏移(real、real)。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>层矩形始终包括`extend=`所做的任何修改。

定义图层矩形的对齐点，该矩形用于通过`pos=`相对于图层0定位图层矩形。 `originN=0,0` 将图层来源放在图层矩形的中心。`originN=-0.5,-0.5` 和 `origin=0,0` 左上角，也 `originN=0.5,0.5` 是图层矩形的右下角。

## 属性 {#section-60f639e36ada43d1abc6bfc100afc925}

图层属性。 应用于当前图层，或应用于`layer=comp`时的图层0。 不受应用于图层源的图层变换(`crop=`、`scale=`、`rotate=`、`flip=`)的影响。 覆盖`anchor=`。 被效果图层忽略。

## 默认 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，则通过将图层变换应用于图像锚点来确定图层来源。 如果不知道图像锚点，则使用图层矩形的中心(`originN=0,0`)。

## 示例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
