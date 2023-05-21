---
title: 縮放檢視
description: 在連續縮放模式中，目前資產為單一影像時，主檢視是由可縮放影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 縮放檢視{#zoom-view}

在連續縮放模式中，目前資產為單一影像時，主檢視是由可縮放影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7mixedmediaviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 主檢視的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標 </span> </p> </td> 
   <td colname="col2"> <p>游標顯示在主檢視上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 使縮放檢視透明。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌上型電腦系統上，元件支援 `cursortype` 屬性選擇器，可套用至 `.s7zoomview` 類別。 它根據元件狀態和使用者動作來控制游標型別。 下列專案 `cursortype` 支援的值：

* `default`

   當影像因影像解析度或元件設定（或兩者）較小而無法縮放時顯示。

* `zoomin`

   影像可放大時顯示。

* `reset`

   當影像處於最大縮放等級時顯示，並可重設為初始狀態。

* `drag`

   當使用者平移處於已縮放狀態的影像時顯示。

* `slide`

   當使用者執行水準撥動或輕觸來執行影像交換時顯示。
