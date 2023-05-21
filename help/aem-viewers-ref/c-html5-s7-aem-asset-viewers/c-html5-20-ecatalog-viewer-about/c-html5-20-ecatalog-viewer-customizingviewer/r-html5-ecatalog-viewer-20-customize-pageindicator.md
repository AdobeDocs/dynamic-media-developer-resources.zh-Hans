---
title: 頁面指標
description: 頁面指示器會顯示目前的頁面索引和總頁面計數。 它會顯示在桌上型電腦系統和平板電腦的主控制列中，在行動電話上則會新增至次要控制列。 頁面指標可由CSS調整大小、建立外觀和定位。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 4%

---

# 頁面指標{#page-indicator}

頁面指示器會顯示目前的頁面索引和總頁面計數。 它會顯示在桌上型電腦系統和平板電腦的主控制列中，在行動電話上則會新增至次要控制列。 頁面指標可由CSS調整大小、建立外觀和定位。

頁面指示器的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的頂端邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的右邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的左邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主要控制列（在桌上型電腦系統和平板電腦上）或次要控制列（在行動電話上）的底部邊框定位，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>頁面指示器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>頁面指示器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字体颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定頁面指示器為56 x 28畫素、水準置中和從主控列底部放置4畫素，並使用14畫素的Helvetica®字型。

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
