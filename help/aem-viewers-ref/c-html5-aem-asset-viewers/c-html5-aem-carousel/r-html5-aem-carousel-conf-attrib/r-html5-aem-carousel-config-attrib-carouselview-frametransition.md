---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持續時間`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化|幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>指定套用到影格變更的效果型別。 例如， <span class="codeph"> 無 </span> 代表無過渡；畫面格變更會立即發生。 和 </p> <p> <span class="codeph"> 淡化 </span> 表示舊影格和新影格之間的交叉淡化切換。 最後， </p> <p> <span class="codeph"> 幻燈片 </span> 啟動轉變，舊框架滑出檢視，新框架滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p>指定下列專案的持續時間（以秒為單位） <span class="codeph"> 淡化 </span> 或 <span class="codeph"> 幻燈片 </span> 切換效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距 </span> </span> </p> </td> 
   <td colname="col2"> <p>中相鄰影格之間的間距 <span class="codeph"> 幻燈片 </span> 轉變，範圍從 <span class="codeph"> 0 </span> 到 <span class="codeph"> 1 </span> 和相對於元件的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
