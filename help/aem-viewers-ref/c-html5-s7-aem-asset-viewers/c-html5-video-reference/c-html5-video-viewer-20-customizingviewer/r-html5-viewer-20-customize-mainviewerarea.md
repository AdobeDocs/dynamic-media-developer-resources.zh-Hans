---
title: 主要檢視器區域
description: 主檢視區域由視訊佔用。 若未指定大小，通常會設定為符合可用的裝置熒幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 主要檢視器區域{#main-viewer-area}

主檢視區域由視訊佔用。 若未指定大小，通常會設定為符合可用的裝置熒幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

下列CSS類別選取器可控制檢視區域的外觀：

```
.s7videoviewer 
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

若要設定具有白色背景(#FFFFFF)的視訊檢視器，並使其大小為512 x 288畫素：

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
