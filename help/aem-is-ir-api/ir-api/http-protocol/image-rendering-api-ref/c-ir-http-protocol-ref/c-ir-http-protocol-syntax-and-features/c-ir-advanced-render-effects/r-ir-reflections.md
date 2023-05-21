---
title: 思考
description: 可以製作暈映以包含近3D反射資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 思考{#reflections}

可以製作暈映以包含近3D反射資料。

如果這樣創作，則會使用下列材料屬性來定義材料的反射曲面屬性：

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> 光澤=</span> </a> </p> </td> 
   <td> <p>表面光澤度 </p> </td> 
   <td> <p>從暈映 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>光澤變化（灰階影像） </p> </td> 
   <td> <p>无 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> 粗加工= </span> </a> </p> </td> 
   <td> <p>表面粗糙度 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>材質型別 </p> </td> 
   <td> <p>0 （未知） </p> </td> 
  </tr> 
 </tbody> 
</table>

轉譯器會調整 `gloss=` 和 `rough=` 根據的屬性 `type=`. 某些材料型別（例如織物）的反射比材料型別（例如石頭或金屬）的反射少。 此外，為其中一個專案指定的相同光澤量，通常會產生與另一個專案不同的反射效果。 屬性 `gloss=` 和粗糙度有相當寬的色域，如果 `type=` 未指定或設為 `0`.

`glossmap=` 用來逐個畫素控制材料的光澤度。
