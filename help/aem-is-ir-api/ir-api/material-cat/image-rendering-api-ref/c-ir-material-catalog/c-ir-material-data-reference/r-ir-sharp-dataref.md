---
description: 锐化。 锐化属性，确定在渲染过程中何时锐化材料。
solution: Experience Manager
title: 清晰
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 8%

---

# 清晰{#sharp}

锐化。 锐化属性，确定在渲染过程中何时锐化材料。

锐化的类型和数量通过默认材质模板或通过`catalog::RenderSettings`由晕影控制。

## 属性 {#section-aac81b1a611b4bca90b8544eae7896df}

枚举。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>不锐化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>普通锐化（变换后）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>替代锐化（变换前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更锐化（变换前和变换后）。 </p></td> 
 </tr> 
</table>

被纯色材料忽略，对于所有其他材料而言，它是可选的。

## 默认 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

如果该字段不存在、为空，或者该值不是支持的选项之一，则使用`attribute::Sharpening`。

## 另请参阅 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute：：Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ， [catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd)， [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
