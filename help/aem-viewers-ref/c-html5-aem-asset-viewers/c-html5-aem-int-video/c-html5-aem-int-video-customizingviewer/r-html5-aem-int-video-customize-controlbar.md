---
description: 控制栏是一个矩形区域，其中包含并位于视频查看器可用的所有UI控件的后面，例如播放/暂停按钮、音量控件等。
solution: Experience Manager
title: 控制栏
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# 控制栏{#control-bar}

控制栏是一个矩形区域，其中包含并位于视频查看器可用的所有UI控件的后面，例如播放/暂停按钮、音量控件等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用查看器宽度。 可以通过CSS相对于视频查看器容器更改其颜色、高度和垂直位置。

以下CSS类选择器控制控制栏的外观：

```
.s7interactivevideoviewer .s7controlbar
```

## 控制栏的CSS属性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 从下边框的位置，包括内边距。 </p> </td> 
  </tr> 
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

要设置视频查看器，其中的灰色控制栏高度为30像素，并位于视频查看器容器的顶部。

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
