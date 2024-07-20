---
title: 主查看器区域
description: 主视图区域由智能裁剪视频占用。 它通常设置为在没有指定大小时适应可用的设备屏幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c8ea6698-e425-491f-8413-2260ddf40c33
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 主查看器区域{#main-viewer-area}

主视图区域由视频占用。 它通常设置为在没有指定大小时适应可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下CSS类选择器控制查看区域的外观：

```
.s7smartcropvideoviewer 
```

## 主查看器区域的CSS属性 {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>查看器宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>查看器高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有白色背景(#FFFFFF)的智能裁切视频查看器，并使其大小为512 x 288像素，请执行以下操作：

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
