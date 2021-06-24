---
description: 材料表面粗糙度。 指定材料曲面的相对粗糙度。
solution: Experience Manager
title: 粗糙
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# 粗糙{#rough}

材料表面粗糙度。 指定材料曲面的相对粗糙度。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>表面粗糙度(0...100%)或–1来选择缺省粗糙度。 </p> </td> 
 </tr> 
</table>

用于控制3D反射渲染效果。 较低的粗糙度值通常会产生更平滑的反射效果；值越高，反射图像的随机化和散射就越大。

每种材料类型(`type=`)根据粗糙度定义最小和最大反射渲染效果。 对于某些材料类型（如墙纸），`rough=`对反射的外观几乎没有任何影响，而对于其他材料类型（如石材或陶瓷），效果显着。

`rough=-1` 将粗糙度设置为服务器内部默认值（典型材料类型为40%）。

## 属性 {#section-515375758b254c80af576271bdb61bb8}

材料属性。 如果晕影没有3D反射功能，目标对象没有与其关联的3D几何，或者目标对象没有反映场景中的任何其他对象，则忽略此问题。

## 默认 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 如果材料基于目录条目，则其他约40%。

## 另请参阅 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
