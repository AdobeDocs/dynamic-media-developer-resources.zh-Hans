---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

指定元件區域中色票容器的內部對齊（錨點）。 在「色票」中，會調整內部縮圖容器的大小，以只顯示整數的色票。 因此，內部容器和外部元件邊界間會有一段邊距。 此命令會指定如何將內部色票容器放置在元件內。

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> 設定水準色票的對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> 設定垂直色票的對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`center,center`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
