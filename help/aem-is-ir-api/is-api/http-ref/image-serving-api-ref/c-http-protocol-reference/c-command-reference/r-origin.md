---
title: 来源
description: 图层原点。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
TQID: 'https://experienceleague.adobe.com/-wkJjmR-LwxC90IMLNXldXSiaugkaYRyvLS17-nbJAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 2%

---

# 来源{#origin}

图层原点。

`origin= *`列`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">坐标</span> </p></td> 
  <td class="stentry"> <p>从图层矩形左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从图层矩形中心的规范化偏移（实际、实际）。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>该图层矩形始终包含由`extend=`进行的任何修改。

定义图层矩形的对齐点，用于通过`pos=`相对于图层0定位图层矩形。 `originN=0,0`将图层原点定位在图层矩形的中心。 `originN=-0.5,-0.5`和`origin=0,0`是左上角，`originN=0.5,0.5`是图层矩形的右下角。

## 属性 {#section-60f639e36ada43d1abc6bfc100afc925}

层属性。 应用于当前图层，或应用于图层0（如果为`layer=comp`）。 不受应用到层源的层转换(`crop=`、`scale=`、`rotate=`、`flip=`)的影响。 覆盖`anchor=`。 被效果层忽略。

## 默认 {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

如果未指定`origin=`，则通过将图层变换应用于图像锚点来确定图层原点。 如果不知道图像锚点，则使用图层矩形(`originN=0,0`)的中心。

## 示例 {#section-13e38d6e17be4e6cbc6b27fbde63b291}

查看[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
