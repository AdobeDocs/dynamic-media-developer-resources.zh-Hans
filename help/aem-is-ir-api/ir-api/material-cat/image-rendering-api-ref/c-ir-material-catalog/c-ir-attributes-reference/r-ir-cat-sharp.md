---
description: 默认材质锐化。 在特定目录记录不包含有效目录锐化值时设置默认材料锐化模式。
seo-description: 默认材质锐化。 在特定目录记录不包含有效目录锐化值时设置默认材料锐化模式。
seo-title: 清晰
solution: Experience Manager
title: 清晰
uuid: f6a6101c-3d9e-4557-892b-be7943b4fdca
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---


# 锐化 {#sharp}

默认材质锐化。 在特定目录记录不包含有效目录：:Sharp值时设置默认的材料锐化模式。

## 属性 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

枚举。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>更多锐化（在变换之前和之后）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-613130fca7c04ce7a7734265f27aa1ea}

如果未定义或为空，则从`default::Sharp`继承。

## 另请参阅 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a),  [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
