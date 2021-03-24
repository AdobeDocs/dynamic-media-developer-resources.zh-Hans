---
description: 控制栏是一个矩形区域，它包含并位于可用于视频查看器的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。
solution: Experience Manager
title: 控制栏
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 控制栏{#control-bar}

控制栏是一个矩形区域，它包含并位于可用于视频查看器的所有用户界面控件（如播放/暂停按钮、音量控件等）的后面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用查看器宽度。 可以通过CSS更改其颜色、高度和垂直位置(相对于视频查看器容器)。

以下CSS类选择器控制控件条的外观：

```
.s7mixedmediaviewer .s7controlbar
```

## 控件条{#css-properties-of-the-control-bar}的CSS属性

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>控件条的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

设置高度为30像素的灰色控制栏的混合媒体查看器。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

