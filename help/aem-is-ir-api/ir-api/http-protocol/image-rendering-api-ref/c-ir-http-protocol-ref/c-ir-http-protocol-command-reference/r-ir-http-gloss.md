---
title: 光泽
description: 材料表面光泽度。 指定材料曲面的相对光泽度。 用于选择照明地图和控制光泽效果和3D反射的渲染。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 光泽{#gloss}

材料表面光泽度。 指定材料曲面的相对光泽度。 用于选择照明地图和控制光泽效果和3D反射的渲染。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>光泽值(0...100%)或–1(默认（参考）光泽值)。 </p></td> 
 </tr> 
</table>

较高的光泽值通常会导致更强、更锐利的反射，并且，如果在晕影中启用光泽效果，则主要通过增加光照对比度来增强材料表面上的镜面亮部。 每种材质类型( `type=`)定义最小和最大渲染效果。 对于某些材料类型（例如，墙纸）， `gloss=` 对渲染效果外观的任何影响最小，而对于其他材料类型（例如石材或陶瓷），效果明显更明显。

如果 `illum=-1` 如果晕影定义了多个照明地图， `gloss=` 选择用于当前渲染操作的照明地图。 渲染器选择其光泽值最接近指定光泽的照明映射。

`gloss=-1` 选择所选照明地图的参考光泽值，如晕影的视图属性中所定义。 此值可确保照度图完全按照创作方式使用，无需进一步修改，即使启用了光泽效果也是如此。 如果 `illum=-1` 然后，使用晕映视图中的第一照明地图的参考光泽值。

## 属性 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

材质属性。 如果晕影未定义多个照明映射，则忽略。 或者，如果 `illum=` 如果晕影不包含3D反射数据，则指定。 或者，如果当前对象不支持3D反射，或者在晕影中禁用光泽效果。

## 默认 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 如果材料基于目录条目，否则，缺省照明地图的参考光泽值或指定的照明地图 `illum=`.

## 另请参阅 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute：：Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)， [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)， [粗加工=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)， [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)， [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
