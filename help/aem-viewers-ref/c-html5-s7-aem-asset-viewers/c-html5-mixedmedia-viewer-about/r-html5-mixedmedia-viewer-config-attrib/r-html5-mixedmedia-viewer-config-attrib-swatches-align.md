---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4f25112b-9e51-4a0e-9500-1b5ab0f4de87
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
