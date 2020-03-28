---
description: 可创作晕影以包含近3D反射数据。
seo-description: 可创作晕影以包含近3D反射数据。
seo-title: 反射
solution: Experience Manager
title: 反射
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 反射{#reflections}

可创作晕影以包含近3D反射数据。

如果创作了该属性，则使用以下材料属性来定义材料的反射表面属性：

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> 光泽=</span></a> </p> </td> 
   <td> <p>表面光泽度 </p> </td> 
   <td> <p>从暗角 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glosmap= </span></a> </p> </td> 
   <td> <p>光泽变化（灰度图像） </p> </td> 
   <td> <p>无 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> 粗糙= </span></a> </p> </td> 
   <td> <p>表面粗糙度 </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> 类型=</span></a> </p> </td> 
   <td> <p>材料类型 </p> </td> 
   <td> <p>0（未知） </p> </td> 
  </tr> 
 </tbody> 
</table>

呈示器根据调整属 `gloss=` 性 `rough=` 的范围 `type=`。 某些材料类型如织物通常比诸如石头或金属之类的材料类型的反射性小，并且为一种材料指定的相同光泽量将导致不同于另一种材料的反射效果。 `gloss=`如果未指定或设置为0，则粗 `type=` 度具有相当宽的色域。

`glossmap=` 可用于逐个像素地控制材料的光泽度。
