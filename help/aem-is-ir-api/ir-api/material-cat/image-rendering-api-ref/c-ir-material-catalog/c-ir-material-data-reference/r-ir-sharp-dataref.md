---
description: 锐化. 锐化属性，确定渲染期间锐化素材的时间。
seo-description: 锐化. 锐化属性，确定渲染期间锐化素材的时间。
seo-title: 清晰
solution: Experience Manager
title: 清晰
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 锐化 {#sharp}

锐化. 锐化属性，确定渲染期间锐化素材的时间。

锐化的类型和数量由暗角通过默认材料模板或与一起控制 `catalog::RenderSettings`。

## 属性 {#section-aac81b1a611b4bca90b8544eae7896df}

枚举。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>无需锐化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>正常锐化（转换后）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代锐化（在变换之前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更多锐化（变换前后）。 </p></td> 
 </tr> 
</table>

被纯色材料忽略，对于所有其他材料为可选。

## 默认 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 如果字段不存在、为空或值不是支持的选项之一，则使用。

## 另请参阅 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[属性：：锐化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ，目 [录：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
