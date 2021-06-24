---
description: 层原点。
solution: Experience Manager
title: 来源
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 来源{#origin}

层原点。

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>从图层直角的左上角(int， int)偏移像素。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>与层矩形中心的标准化偏移（实、实）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>层矩形始终包含`extend=`的任何修改。

定义层矩形的对齐点，该对齐点用于通过`pos=`相对于层0定位层矩形。 `originN=0,0` 将层原点放置在层矩形的中心。`originN=-0.5,-0.5` 和 `origin=0,0` 位于图层矩形的 `originN=0.5,0.5` 左上角和右下角。

## 属性 {#section-60f639e36ada43d1abc6bfc100afc925}

层属性。 应用于当前层，或在`layer=comp`时应用于层0。 不受应用于层源的层转换(`crop=`、`scale=`、`rotate=`、`flip=`)的影响。 覆盖`anchor=`。 被效果层忽略。

## 默认 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，则通过将层变换应用于图像锚点来确定层原点。 如果图像锚点未知，则使用层矩形的中心(`originN=0,0`)。

## 示例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

请参阅[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
