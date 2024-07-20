---
title: 反射
description: 可以创作晕影以包含近3D反射数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# 反射{#reflections}

可以创作晕影以包含近3D反射数据。

如果这样创作，则可使用以下材料属性来定义材料的反射曲面属性：

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
   <th class="entry"> <p>默认 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph">光泽=</span> </a> </p> </td> 
   <td> <p>表面光泽度 </p> </td> 
   <td> <p>从晕影 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph">词汇表= </span> </a> </p> </td> 
   <td> <p>光泽变量（灰度图像） </p> </td> 
   <td> <p>无 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph">粗略= </span> </a> </p> </td> 
   <td> <p>表面粗糙度 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph">类型=</span> </a> </p> </td> 
   <td> <p>材质类型 </p> </td> 
   <td> <p>0（未知） </p> </td> 
  </tr> 
 </tbody> 
</table>

渲染器根据`type=`调整`gloss=`和`rough=`属性的范围。 某些材料类型（如织物）的反射比材料类型（如石材或金属）少。 此外，为某一面指定的相同光泽量通常导致与另一面不同的反射效果。 如果未指定`type=`或将其设置为`0`，则属性`gloss=`和粗糙度具有相当宽的色域。

`glossmap=`用于逐像素控制材料的光泽度。
