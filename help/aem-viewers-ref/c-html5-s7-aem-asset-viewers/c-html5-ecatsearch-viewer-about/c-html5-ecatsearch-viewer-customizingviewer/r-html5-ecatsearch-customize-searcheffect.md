---
title: 搜尋效果
description: 檢視器會在主檢視上顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# 搜尋效果{#search-effect}

檢視器會在主檢視上顯示搜尋結果區域，以反白標示在目錄中找到的字詞或片語。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

搜尋結果區域的外觀由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>搜尋結果區域的背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定具有半透明、黃色填色的搜尋結果區域：

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
