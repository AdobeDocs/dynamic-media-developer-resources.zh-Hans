---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`限制`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[，<span class="varname">限制</span>]</span> </p> </td> 
   <td colname="col2"> <p> 根据页数和运行时组件大小配置自动隐藏行为。 </p> <p> <span class="codeph"> 0</span>关闭自动隐藏。 </p> <p> <span class="codeph"> 1</span>启用自动隐藏。 如果满足以下至少一个条件，则组件将隐藏其圆点： </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">带点的行变得比运行时组件宽度更宽，或 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">为此组件设置的页数超过了<span class="codeph"><span class="varname"> limit</span></span>参数配置的限制。 </li> 
     </ul> </p> <p> 将<span class="codeph"><span class="varname">限制</span></span>设置为<span class="codeph"> -1</span>将禁用第二个自动隐藏条件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
