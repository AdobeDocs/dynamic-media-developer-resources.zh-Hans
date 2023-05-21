---
title: 控制列
description: 控制列是一個矩形區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如「播放/暫停」按鈕、音量控制項等。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# 控制列{#control-bar}

控制列是一個矩形區域，其中包含並位於所有可用於視訊檢視器的使用者介面控制項後面，例如「播放/暫停」按鈕、音量控制項等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制列總是取用整個可用的檢視器寬度。 您可以透過CSS變更其相對於視訊檢視器容器的顏色、高度和垂直位置。

下列CSS類別選擇器會控制控制列的外觀：

```
.s7mixedmediaviewer .s7controlbar
```

## 控制列的CSS屬性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>控制列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要使用高度為30畫素的灰色控制列來設定混合媒體檢視器。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
