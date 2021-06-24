---
description: 控制栏是矩形区域，其中包含并位于视频查看器可用的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。
solution: Experience Manager
title: 控制栏
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 控制栏{#control-bar}

控制栏是矩形区域，其中包含并位于视频查看器可用的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用查看器宽度。 可以通过CSS相对于视频查看器容器更改其颜色、高度和垂直位置。

以下CSS类选择器控制控制栏的外观：

```
.s7mixedmediaviewer .s7controlbar
```

## 控制栏的CSS属性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>控制栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置高度为30像素的灰色控制栏的混合媒体查看器，请执行以下操作：

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
