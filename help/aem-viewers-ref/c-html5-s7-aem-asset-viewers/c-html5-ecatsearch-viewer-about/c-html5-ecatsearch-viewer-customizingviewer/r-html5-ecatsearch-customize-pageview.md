---
title: 页面查看
description: 主檢視由目錄影像組成。 它可以輕掃以進入另一個頁面或縮放。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 4%

---

# 页面查看{#page-view}

主檢視由目錄影像組成。 它可以輕掃以進入另一個頁面或縮放。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> 主檢視的背景顏色（以十六進位格式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 游標 </span> </p> </td> 
   <td colname="col2"> <p>顯示在主檢視上的游標。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 讓主檢視透明。

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

在桌上型電腦系統上，元件支援 `cursortype` 可套用到的屬性選擇器 `.s7pageview` 類別並根據元件狀態和使用者動作控制游標型別。 下列專案 `cursortype` 支援的值：

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 默认 </span> </p> </td> 
   <td colname="col2"> <p>因影像解析度小、元件設定或兩者而不可縮放時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 縮放 </span> </p> </td> 
   <td colname="col2"> <p>影像可放大時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重置 </span> </p> </td> 
   <td colname="col2"> <p>當影像處於最大縮放等級時顯示，並可重設為初始狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖动 </span> </p> </td> 
   <td colname="col2"> <p>當使用者平移處於已縮放狀態的影像時顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>當使用者執行水準撥動或輕觸來執行影像交換時顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

視覺上分隔目錄跨頁左右頁面的頁面分隔線，由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 頁面分隔線的寬度。 設定為 <span class="codeph"> 0 </span> px以完全隱藏分隔線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>您要用作頁面分隔線的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 具有40畫素的寬分頁器，含半透明影像。

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>當 `frametransition` 修飾元設為 `turn` 或 `auto` （在桌上型電腦系統上），分頁器的外觀是由 `pageturnstyle` 修飾元與 `.s7pagedivider` 已忽略CSS類別。

您可在主要檢視器區域上設定自訂滑鼠游標顯示。 此功能由套用到的其他屬性選擇器控制 `.s7ecatalogsearchviewer .s7pageview` CSS類別：

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 默认 </span> </p> </td> 
   <td colname="col2"> <p> 通常為箭頭，會顯示不可縮放的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 縮放 </span> </p> </td> 
   <td colname="col2"> <p> 顯示何時可以放大影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重置 </span> </p> </td> 
   <td colname="col2"> <p>顯示影像何時達到最大縮放並可重設。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖动 </span> </p> </td> 
   <td colname="col2"> <p>顯示使用者何時對已縮放的影像執行拖曳操作 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>顯示使用者使用投影片手勢執行影像交換的時間 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 每種元件狀態的滑鼠游標型別不同。

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
