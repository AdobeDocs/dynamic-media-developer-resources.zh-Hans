---
title: 傳送檢視
description: 主要檢視包含橫幅影像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: aa41b209-11c7-4744-aaa5-dc0b503607c6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 1%

---

# 傳送檢視{#carousel-view}

主要檢視包含橫幅影像。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7carouselviewer .s7carouselview
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
 </tbody> 
</table>

範例 — 讓主檢視透明。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```
