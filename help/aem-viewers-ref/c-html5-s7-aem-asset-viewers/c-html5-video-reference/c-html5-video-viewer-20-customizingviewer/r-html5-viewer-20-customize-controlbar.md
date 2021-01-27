---
description: 控制栏是一个矩形区域，它包含并位于视频查看器可用的所有UI控件（如播放／暂停按钮、音量控件等）的后面。
seo-description: 控制栏是一个矩形区域，它包含并位于视频查看器可用的所有UI控件（如播放／暂停按钮、音量控件等）的后面。
seo-title: 控制栏
solution: Experience Manager
title: 控制栏
topic: Dynamic Media
uuid: 5686b670-3c8c-4bef-b428-dc468f6ca05d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# 控制栏{#control-bar}

控制栏是一个矩形区域，它包含并位于视频查看器可用的所有UI控件（如播放／暂停按钮、音量控件等）的后面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用查看器宽度。 可以通过CSS更改其颜色、高度和垂直位置(相对于视频查看器容器)。

以下CSS类选择器控制控件条的外观：

```
.s7videoviewer .s7controlbar
```

## 控件条{#css-properties-of-the-control-bar}的CSS属性

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 从底部边框开始的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置一个视频查看器，其中灰色控件条高度为30像素，并位于视频查看器容器的顶部。

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

