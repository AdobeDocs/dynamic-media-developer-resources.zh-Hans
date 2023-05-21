---
title: 主要檢視器區域
description: 主要檢視區域是縮放影像和色票所佔用的區域。 若未指定大小，通常會設定為符合可用的裝置熒幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# 主要檢視器區域{#main-viewer-area}

主要檢視區域是縮放影像和色票所佔用的區域。 若未指定大小，通常會設定為符合可用的裝置熒幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

在嵌入模式下工作時（當為主檢視器區域指定明確大小時），檢視器會自動根據處理單一影像的「色票」元件高度來減少其主要區域的高度，因此不需要色票。

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7zoomviewer
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

範例 — 設定具有白色背景的檢視器( `#FFFFFF`)，並將其大小設為512 x 288畫素。

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
