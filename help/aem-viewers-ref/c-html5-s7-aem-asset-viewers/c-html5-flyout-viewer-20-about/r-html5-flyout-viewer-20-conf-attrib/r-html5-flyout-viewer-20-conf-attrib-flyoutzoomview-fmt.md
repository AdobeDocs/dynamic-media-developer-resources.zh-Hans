---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 4e1ce754-6967-492b-a617-764ee3ec3a55
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件從影像伺服器載入影像時所用的影像格式。 如果指定的格式結尾為 <span class="codeph"> "-alpha"</span>，元件會將影像呈現為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 元件預設為白色背景。 因此，若要使其透明，請設定 <span class="codeph"> background-color</span> CSS屬性至 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
