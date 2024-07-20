---
title: 缩放视图
description: 主视图由可缩放图像组成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 缩放视图{#zoom-view}

主视图由可缩放图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 主视图的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">游标</span> </p> </td> 
   <td colname="col2"> <p>光标显示在主视图上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌面系统上，该组件支持`cursortype`属性选择器，该选择器可以应用于`.s7zoomview`类。 它根据组件状态和用户操作控制光标的类型。 支持以下`cursortype`值：

* `default`

  由于图像分辨率或组件设置太小或两者同时存在而导致图像无法缩放时显示。

* `zoomin`

  在可以放大图像时显示。

* `reset`

  当图像处于最大缩放级别时显示，并且可以重置为其初始状态。

* `drag`

  当用户平移处于放大状态的图像时显示。

* `slide`

  当用户通过执行水平轻扫或轻扫执行图像交换时显示。
