---
description: 控件栏是矩形区域，它包含和位于视频查看器可用的所有用户界面控件（如播放／暂停按钮、音量控件等）的后面。
seo-description: 控件栏是矩形区域，它包含和位于视频查看器可用的所有用户界面控件（如播放／暂停按钮、音量控件等）的后面。
seo-title: 控制栏
solution: Experience Manager
title: 控制栏
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 控制栏{#control-bar}

控件栏是矩形区域，它包含和位于视频查看器可用的所有用户界面控件（如播放／暂停按钮、音量控件等）的后面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用整个可用的查看器宽度。 可以通过CSS更改其颜色、高度和垂直位置(相对于视频查看器容器)。

以下CSS类选择器控制控件条的外观：

```
.s7video360viewer .s7controlbar
```

## 控件栏的CSS属性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框开始的位置，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 从底部边框开始的位置，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** -设置一个视频查看器，其中灰色控件条高度为30像素，位于视频查看器容器的顶部。

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

