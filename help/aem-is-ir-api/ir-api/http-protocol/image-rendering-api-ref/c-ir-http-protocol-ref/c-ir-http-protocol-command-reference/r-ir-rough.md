---
description: 材料表面粗糙度。 指定材料表面的相对粗糙度。
seo-description: 材料表面粗糙度。 指定材料表面的相对粗糙度。
seo-title: 粗糙
solution: Experience Manager
title: 粗糙
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# rough{#rough}

材料表面粗糙度。 指定材料表面的相对粗糙度。

` rough= *`瓦尔`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 瓦尔  </span> </p> </td> 
  <td class="stentry"> <p>表面粗糙度(0...100%)或–1以选择缺省粗糙度。 </p> </td> 
 </tr> 
</table>

用于控制3D反射渲染效果。 较低的粗糙度值通常会产生更平滑的反射效果；值越高，反射图像的随机化和散射就越严重。

每种材料类型(`type=`)根据粗糙度定义最小和最大反射渲染效果。 对于某些材料类型（例如墙纸），`rough=`对反射的外观几乎没有任何影响，而对于其他材料类型（例如石头或陶瓷），其影响显着。

`rough=-1` 将粗糙度设置为服务器内部默认值（典型材料类型为40%）。

## 属性 {#section-515375758b254c80af576271bdb61bb8}

材料属性。 如果晕影没有3D反射功能，如果目标对象没有与其关联的3D几何，或者目标对象没有反映场景中的任何其他对象，则忽略。

## 默认 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 如果材料基于目录条目，则其他情况约为40%。

## 另请参阅 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
