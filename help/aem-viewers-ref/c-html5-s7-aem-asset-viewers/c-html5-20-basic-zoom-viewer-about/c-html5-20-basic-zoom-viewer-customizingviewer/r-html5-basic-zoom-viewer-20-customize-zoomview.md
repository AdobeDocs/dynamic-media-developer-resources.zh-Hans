---
description: 主视图由可缩放图像组成。
seo-description: 主视图由可缩放图像组成。
seo-title: 缩放视图
solution: Experience Manager
title: 缩放视图
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 3%

---


# 缩放视图{#zoom-view}

主视图由可缩放图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p>光标显示在主视图上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

在桌面系统上，组件支持`cursortype`属性选择器，该选择器可应用于`.s7zoomview`类，并根据组件状态和用户操作控制游标类型。 支持以下`cursortype`值：

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 默认 </span> </p> </td> 
   <td colname="col2"> <p>当图像因图像分辨率较低或组件设置或两者兼有而无法缩放时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 卓敏  </span> </p> </td> 
   <td colname="col2"> <p>当图像可以放大时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重置 </span> </p> </td> 
   <td colname="col2"> <p>当图像处于最大缩放级别时显示，并可重置为其初始状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖动 </span> </p> </td> 
   <td colname="col2"> <p>当用户平移处于缩放状态的图像时显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

