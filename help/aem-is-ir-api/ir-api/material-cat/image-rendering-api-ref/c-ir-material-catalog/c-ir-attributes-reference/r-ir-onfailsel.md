---
title: OnFailSel
description: 选取选区错误处理。 指定sel=命令因指定的像素位置不在可选对象的蒙版区域中而失败时应采取的操作。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# OnFailSel{#onfailsel}

选取选区错误处理。 指定由于指定的像素位置不在可选对象的蒙版区域中而导致`sel=`命令失败时应采取的操作。

## 属性 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

枚举。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>继承自<span class="codeph">默认值：：OnFailSel </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留以前的选择。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消选择；忽略任何应用材料或显示/隐藏对象的尝试。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>返回错误。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择默认组（晕影层次结构中包含可渲染对象的第一个组）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-c25f458f9f8f4236963a95779529e664}

如果未定义，则从`default::OnFailSel`继承。

## 另请参阅 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ， [attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
