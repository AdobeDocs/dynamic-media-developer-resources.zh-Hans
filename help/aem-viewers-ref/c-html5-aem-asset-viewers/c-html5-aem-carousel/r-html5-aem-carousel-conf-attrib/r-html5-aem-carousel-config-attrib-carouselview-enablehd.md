---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 一律|永不|限制</span> </p> </td> 
   <td colname="col2"> <p> 啟用、限制或停用裝置的最佳化，其中 <span class="codeph"> devicePixelRatio</span> 大於 <span class="codeph"> 1</span>，也就是具有高密度顯示器的裝置，例如iPhone4和類似裝置。 </p> <p>如果啟用，則元件會限制IS影像請求的大小，彷彿裝置的畫素比僅為 <span class="codeph"> 1</span> 進而減少頻寬。 </p> <p>請參閱以下範例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 若使用 <span class="codeph"> 限制</span> 設定時，元件僅會啟用指定上限的高畫素密度。 </p> <p>請參閱以下範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
