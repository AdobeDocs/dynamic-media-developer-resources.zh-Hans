---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: d9db34f3-66df-45c2-9727-bdcdf09773db
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

指定元件區域中色票容器的內部對齊（錨點）。 在「色票」中，會調整內部縮圖容器的大小，以只顯示整數的色票。 因此，內部容器和外部元件邊界間會有一段邊距。 此命令會指定如何將內部色票容器放置在元件內。

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> 設定水準色票對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td colname="col2"> <p> 設定垂直色票對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`center,center`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`align=left,top`
