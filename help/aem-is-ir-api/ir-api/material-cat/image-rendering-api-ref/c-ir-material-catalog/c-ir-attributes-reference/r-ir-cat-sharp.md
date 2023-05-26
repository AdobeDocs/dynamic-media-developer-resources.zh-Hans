---
title: 清晰
description: 默认材质锐化。 设置特定目录记录中不包含有效目录“锐化”值时的默认材质锐化模式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---

# 清晰{#sharp}

默认材质锐化。 设置特定目录记录中不包含有效内容时的默认材质锐化模式 `catalog::Sharp` 值。

## 属性 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

枚举。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>更锐化（变换前和变换后）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-613130fca7c04ce7a7734265f27aa1ea}

继承自 `default::Sharp` 如果未定义或为空。

## 另请参阅 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog：：锐化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ， [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)， [catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
