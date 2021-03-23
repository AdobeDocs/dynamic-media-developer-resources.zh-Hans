---
description: 选取选择错误处理。 指定sel=命令失败时要执行的操作，因为指定的像素位置不在可选对象的蒙版区域内。
seo-description: 选取选择错误处理。 指定sel=命令失败时要执行的操作，因为指定的像素位置不在可选对象的蒙版区域内。
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 10%

---


# OnFailSel{#onfailsel}

选取选择错误处理。 指定sel=命令失败时要执行的操作，因为指定的像素位置不在可选对象的蒙版区域内。

## 属性 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

枚举。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>继承自<span class="codeph">默认值：:OnFailSel </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留以前的选择. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消选择；将忽略应用材料或显示/隐藏对象的任何尝试。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>返回错误. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择默认组（晕影层次结构中包含可渲染对象的第一个组）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-c25f458f9f8f4236963a95779529e664}

如果未定义，则从`default::OnFailSel`继承。

## 另请参阅 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ，属 [性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
