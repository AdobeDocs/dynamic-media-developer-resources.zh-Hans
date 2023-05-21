---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f13faa03-3b69-4cae-aaf5-55edd4aa5c84
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件從影像伺服器載入影像時所用的影像格式。 如果指定的格式結尾為 <span class="codeph"> -alpha</span>，元件會將影像呈現為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 元件預設為白色背景。 因此，若要使其透明，請設定 <span class="codeph"> background-color</span> CSS屬性至 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
