---
title: 迴轉檢視
description: 目前資產為迴轉集時，主檢視會由迴轉影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# 迴轉檢視{#spin-view}

目前資產為迴轉集時，主檢視會由迴轉影像組成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> 迴轉檢視的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 使迴轉檢視透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
