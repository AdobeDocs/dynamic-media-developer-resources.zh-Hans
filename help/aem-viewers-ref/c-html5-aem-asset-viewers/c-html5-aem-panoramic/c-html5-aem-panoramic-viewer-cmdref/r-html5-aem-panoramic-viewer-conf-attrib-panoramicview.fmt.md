---
title: PanoramicView.fmt
description: 指定元件從影像伺服器載入影像時，所使用的影像格式。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

指定元件從影像伺服器載入影像時，所使用的影像格式。 如果指定的格式結尾為&quot;-alpha&quot;，元件會將影像呈現為透明。 至於所有其他影像格式，元件會將影像視為不透明。 請注意，元件預設為透明背景。 因此，若要使其不透明，請將 `background-color` CSS屬性至 `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> 指定元件從影像伺服器載入影像時所用的影像格式。 如果指定的格式結尾為"-alpha"，元件會將影像呈現為透明內容，至於所有其他影像格式，元件會將影像視為不透明。 請注意，元件預設為透明背景，因此為了不透明，請將background-color CSS屬性設定為所要的顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
