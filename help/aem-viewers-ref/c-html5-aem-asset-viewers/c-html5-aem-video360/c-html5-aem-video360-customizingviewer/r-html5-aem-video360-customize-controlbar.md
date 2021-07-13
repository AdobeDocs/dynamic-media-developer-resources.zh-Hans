---
description: 控制栏是矩形区域，其中包含并位于视频查看器可用的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。
solution: Experience Manager
title: 控制栏
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# 控制栏{#control-bar}

控制栏是矩形区域，其中包含并位于视频查看器可用的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用查看器宽度。 可以通过CSS相对于视频查看器容器更改其颜色、高度和垂直位置。

以下CSS类选择器控制控制栏的外观：

```
.s7video360viewer .s7controlbar
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

**示例**  — 设置一个视频查看器，其中的灰色控制栏高度为30像素，并位于视频查看器容器的顶部。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
