---
title: 粗加工
description: 材料表面粗糙度。 指定材料表面的相对粗糙度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# 粗加工{#rough}

材料表面粗糙度。 指定材料表面的相对粗糙度。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>表面粗糙度(0...100%)或–1，以选取缺省粗糙度。 </p> </td> 
 </tr> 
</table>

用于控制3D反射渲染效果。 粗糙度值越低，反射效果越平滑；粗糙度值越高，反射图像的随机性和散射性越好。

每种材料类型(`type=`)都定义了基于粗糙度的最小和最大反射渲染效果。 对于某些材料类型（例如，墙纸），`rough=`对反射外观的任何影响最小，而对于其他材料类型（例如，石材或陶瓷），效果则明显更明显。

`rough=-1`将粗糙度设置为服务器内部的默认值（对于典型材料类型，为40%）。

## 属性 {#section-515375758b254c80af576271bdb61bb8}

材质属性。 如果晕影没有3D反射功能、目标对象没有与其关联的3D几何，或者目标对象没有反射场景中的任何其他对象，则忽略该项。

## 默认 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness`如果材料基于目录条目，否则大约为40%。

## 另请参阅 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[类型=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ， [光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
