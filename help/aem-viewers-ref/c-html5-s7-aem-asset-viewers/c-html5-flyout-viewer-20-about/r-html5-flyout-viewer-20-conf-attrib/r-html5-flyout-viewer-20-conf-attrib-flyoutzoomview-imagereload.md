---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。 </p> <p>當設定為 <span class="codeph"> 0 </span>時，元件不會在調整大小期間載入新影像；彈出式檢視中的影像解析度不會變更。 </p> <p>設定為 <span class="codeph"> 1 </span> 可讓您為載入至主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 中斷點， <span class="varname"> 寬度 </span>[； <span class="varname"> 寬度 </span>] </span> </p> </td> 
   <td colname="col2"> <p> 載入主檢視之影像的寬度中斷點。 元件一律會使用最佳配合大小來初始載入。 調整大小後，可確保下載主檢視中的影像時，寬度始終等於最接近的大型中斷點，並在使用者端上縮小比例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
