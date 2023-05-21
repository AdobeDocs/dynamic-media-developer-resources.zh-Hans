---
title: FlyoutZoomView.fmt
description: 指定元件從影像伺服器載入影像時所用的影像格式。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

指定元件從影像伺服器載入影像時所用的影像格式。

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 如果指定的格式結尾為 <span class="codeph"> -alpha</span>，元件會將影像呈現為透明內容。 至於所有其他影像格式，元件會將影像視為不透明。 </p> <p>元件預設為白色背景。 因此，若要使其透明，請設定 <span class="codeph"> background-color</span> CSS屬性至 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
