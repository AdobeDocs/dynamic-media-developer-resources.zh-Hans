---
title: 主要檢視器區域
description: 主要檢視區域由智慧型裁切視訊佔用。 若未指定大小，通常會設定為符合可用的裝置熒幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c8ea6698-e425-491f-8413-2260ddf40c33
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# 主要檢視器區域{#main-viewer-area}

主檢視區域由視訊佔用。 若未指定大小，通常會設定為符合可用的裝置熒幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

下列CSS類別選取器可控制檢視區域的外觀：

```
.s7smartcropvideoviewer 
```

## 主要檢視器區域的CSS屬性 {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視器寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>檢視器高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定具有白色背景(#FFFFFF)的智慧型裁切視訊檢視器，並使其大小為512 x 288畫素：

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
