---
title: 主要檢視器區域
description: 主要檢視區域是輪播橫幅影像所佔用的區域。 若未指定大小，則會設定為符合可用的裝置熒幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# 主要檢視器區域{#main-viewer-area}

主要檢視區域是輪播橫幅影像所佔用的區域。 若未指定大小，則會設定為符合可用的裝置熒幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7carouselviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>檢視器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定具有白色背景的檢視器( `#FFFFFF`)，並將其大小設為1174 x 500畫素。

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
