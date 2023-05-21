---
title: CarouselView.autoplay
description: 轉盤檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 4%

---

# CarouselView.autoplay{#carouselview-autoplay}

轉盤檢視器的設定屬性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][，duration][，direction]</span> </p> </td> 
   <td colname="col2"> <p> 指定開啟/關閉、在輪播中顯示每個橫幅的持續時間以及自動回圈的方向。 </p> <p>設定為 <span class="codeph"> 0</span> 關閉自動回圈。 </p> <p>設定 <span class="codeph"> 1</span> 開啟以秒為單位之轉換持續時間的自動回圈，控制方式為 <span class="codeph"> 持續時間</span>. </p> <p>自動回圈的方向由控制 <span class="codeph"> 方向</span>. 此 <span class="codeph"> 方向</span> 範圍介於 <span class="codeph"> 1</span> 由右至左和 <span class="codeph"> 0</span> 由左至右。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
