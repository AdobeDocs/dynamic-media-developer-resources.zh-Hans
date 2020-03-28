---
description: 在连续缩放模式下，当当前资产是单个图像时，主视图由可缩放图像组成。
seo-description: 在连续缩放模式下，当当前资产是单个图像时，主视图由可缩放图像组成。
seo-title: 缩放视图
solution: Experience Manager
title: 缩放视图
topic: Dynamic media
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

在连续缩放模式下，当当前资产是单个图像时，主视图由可缩放图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

```
.s7mixedmediaviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 以主视图的十六进制格式显示的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 光标 </span> </p> </td> 
   <td colname="col2"> <p>光标显示在主视图上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使缩放视图透明。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌面系统上，该组件支 `cursortype` 持可应用于类的属性选择 `.s7zoomview` 器。 它根据组件状态和用户操作控制光标的类型。 The following `cursortype` values are supported:

* `default`

   当图像因图像分辨率较低或组件设置而无法缩放时显示，或者同时显示。

* `zoomin`

   可放大图像时显示。

* `reset`

   当图像处于最大缩放级别时显示，并可重置为其初始状态。

* `drag`

   当用户平移处于放大状态的图像时显示。

* `slide`

   当用户通过水平轻扫或轻扫执行图像交换时显示。

