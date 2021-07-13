---
description: 对象选择错误处理。 指定当obj=命令失败时要执行的操作，因为指定的路径无法在晕影对象层次结构中匹配。
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 13%

---

# OnFailObj{#onfailobj}

对象选择错误处理。 指定当obj=命令失败时要执行的操作，因为指定的路径无法在晕影对象层次结构中匹配。

## 属性 {#section-2c779d9c133a443d9f0aed9fde7b703c}

枚举。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>从<span class="codeph">默认继承：:OnFailObj </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留以前的选择. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消选择；任何应用材料或显示/隐藏对象的尝试都将被忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>返回错误. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择默认组（晕影层次结构中包含可渲染对象的第一组）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-a5a95a2b4a204a4eae350e5b544d1513}

从`default::OnFailObj`继承（如果未定义）。

## 另请参阅 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ，属 [性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
