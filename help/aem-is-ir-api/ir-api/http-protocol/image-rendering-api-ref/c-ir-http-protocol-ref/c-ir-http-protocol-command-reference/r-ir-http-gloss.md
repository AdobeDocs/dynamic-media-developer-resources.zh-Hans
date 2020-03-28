---
description: 材料表面光泽度。 指定材料表面的相对光泽度。 用于选择照明图并控制光泽效果和3D反射的渲染。
seo-description: 材料表面光泽度。 指定材料表面的相对光泽度。 用于选择照明图并控制光泽效果和3D反射的渲染。
seo-title: 光泽
solution: Experience Manager
title: 光泽
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光泽{#gloss}

材料表面光泽度。 指定材料表面的相对光泽度。 用于选择照明图并控制光泽效果和3D反射的渲染。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>光泽(0...100%)或-1表示默认（参考）光泽值。 </p></td> 
 </tr> 
</table>

较高的光泽值通常导致更强、更锐利的反射，并且如果暗角中启用了光泽效果，则会增强材料表面的镜面高光，主要是通过增加照明对比度。 每种材料类型( `type=`)定义最小和最大渲染效果。 对于某些材料类型（例如墙纸），对渲染效果的外观几乎没有任何影响，而对于其他材料类型（例如，石头或陶瓷），效果显着更明显。 `gloss=`

如果 `illum=-1` 且如果暗角定义了多个照明图，则选择 `gloss=` 用于当前渲染操作的照明图。 渲染器选择其光泽值最接近指定光泽的照明图。

`gloss=-1` 根据暗角的视图属性，选择所选照明图的参考光泽值。 这确保即使启用了光泽效果，照明图也能完全按创作方式使用，无需进一步修改。 如 `illum=-1` 果也这样，则使用暗角视图中第一照明图的参考光泽值。

## 属性 {#section-92c20c7890fc4aad8d1725d1a1f82da6}

材料属性。 如果暗角未定义多个照明映射，或者如果指定，则忽略 `illum=` ，如果暗角不包含3D反射数据，或者如果当前对象不支持3D反射，或者如果暗角中禁用了光泽效果。

## 默认 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` 如果材料基于目录条目，否则默认照明图或由指定的照明图的参考光泽值 `illum=`。

## 另请参阅 {#section-29f5b761481a4c52a499a2e16e63c70b}

[属性：:Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [Glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)[,Glossillum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
