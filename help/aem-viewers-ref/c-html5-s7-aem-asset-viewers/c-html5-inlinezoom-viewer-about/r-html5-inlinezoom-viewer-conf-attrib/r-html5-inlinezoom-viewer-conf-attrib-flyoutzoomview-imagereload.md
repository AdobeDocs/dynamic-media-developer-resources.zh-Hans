---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。 </p> <p>設定為 <span class="codeph"> 0 </span>時，元件不會在調整大小期間載入新影像，而且彈出式檢視中的影像解析度不會變更。 </p> <p>設定為 <span class="codeph"> 1 </span> 可讓您為載入至主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 中斷點， <span class="varname"> 寬度 </span>； <span class="varname"> 寬度 </span> </span> </p> </td> 
   <td colname="col2"> <p>載入主檢視之影像的寬度中斷點。 </p> <p>元件一律會使用最佳配合大小來初始載入。 在調整大小之後，它可確保主檢視中的影像一律使用等於最接近的較大中斷點的寬度下載，並在使用者端上縮放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
