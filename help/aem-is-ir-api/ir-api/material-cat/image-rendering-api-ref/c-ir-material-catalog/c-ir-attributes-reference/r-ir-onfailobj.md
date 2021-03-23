---
description: 对象选择错误处理。 指定当obj=命令由于在晕影对象层次结构中无法匹配指定路径而失败时要执行的操作。
seo-description: 对象选择错误处理。 指定当obj=命令由于在晕影对象层次结构中无法匹配指定路径而失败时要执行的操作。
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---


# OnFailObj{#onfailobj}

对象选择错误处理。 指定当obj=命令由于在晕影对象层次结构中无法匹配指定路径而失败时要执行的操作。

## 属性 {#section-2c779d9c133a443d9f0aed9fde7b703c}

枚举。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>继承自<span class="codeph">默认值：:OnFailObj </span>。 </p> </td> 
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

## 默认 {#section-a5a95a2b4a204a4eae350e5b544d1513}

如果未定义，则从`default::OnFailObj`继承。

## 另请参阅 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [属性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
