---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b02f033d-be84-4cd0-b4bb-3ae9e424680c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预载行为。 当设置为 <span class="codeph"> -1</span> 初始化组件或更改资源时，将同时加载所有样本。 当设置为 <span class="codeph"> 0</span> 仅加载可见样本。 </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> 定义可见区域周围预载多少不可见的行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
