---
description: 锐化. 锐化属性，可确定在渲染期间锐化材料的时间。
solution: Experience Manager
title: 清晰
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 10%

---

# 清晰{#sharp}

锐化. 锐化属性，可确定在渲染期间锐化材料的时间。

锐化的类型和数量由晕影通过默认材料模板或使用`catalog::RenderSettings`进行控制。

## 属性 {#section-aac81b1a611b4bca90b8544eae7896df}

枚举。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>无锐化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>正常锐化（转换后）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>备用锐化（在转换之前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>更多锐化（在转换前后）。 </p></td> 
 </tr> 
</table>

被纯色材料忽略，对于所有其他材料，它是可选的。

## 默认 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 如果字段不存在、为空或值不是支持的选项之一，则使用。

## 另请参阅 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[属性：：锐化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [目录：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
