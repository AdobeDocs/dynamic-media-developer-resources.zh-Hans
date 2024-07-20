---
title: 控件栏
description: 控制栏是一个矩形区域，其中包含并位于视频查看器可用的所有UI控件后面，如播放/暂停按钮和音量控件。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# 控件栏{#control-bar}

控制栏是一个矩形区域，其中包含并位于视频查看器可用的所有UI控件后面，如播放/暂停按钮和音量控件。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用所有可用的查看器宽度。 可以通过CSS更改其相对于视频查看器容器的颜色、高度和垂直位置。

以下CSS类选择器控制控件栏的外观：

```
.s7videoviewer .s7controlbar
```

## 控件栏的CSS属性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p> 下边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>控件栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

设置一个视频查看器，其灰色控制栏高度为30像素，位于视频查看器容器的顶部。

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
