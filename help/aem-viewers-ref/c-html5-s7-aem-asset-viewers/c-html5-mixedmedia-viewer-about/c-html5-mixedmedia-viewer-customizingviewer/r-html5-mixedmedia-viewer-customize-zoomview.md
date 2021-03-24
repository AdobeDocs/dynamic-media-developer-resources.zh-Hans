---
description: 在连续缩放模式下，当当前资产是单个图像时，主视图由可缩放图像组成。
solution: Experience Manager
title: 缩放视图
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# 缩放视图{#zoom-view}

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 主视图的十六进制格式背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 光标  </span> </p> </td> 
   <td colname="col2"> <p>在主视图上显示光标。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使缩放视图透明。

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌面系统上，组件支持`cursortype`属性选择器，该属性选择器可应用于`.s7zoomview`类。 它根据组件状态和用户操作控制光标的类型。 支持以下`cursortype`值：

* `default`

   当图像因图像分辨率较低或组件设置或两者兼有而无法缩放时显示。

* `zoomin`

   当图像可放大时显示。

* `reset`

   当图像处于最大缩放级别时显示，并可重置为其初始状态。

* `drag`

   当用户平移处于缩放状态的图像时显示。

* `slide`

   当用户通过水平轻扫或轻扫执行图像交换时显示。

