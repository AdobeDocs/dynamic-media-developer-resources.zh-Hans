---
title: 主查看器区域
description: 主视图区域被智能裁剪视频占据。 通常在未指定大小时设置为适合可用设备屏幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# 主查看器区域{#main-viewer-area}

主视区域被视频占据。 通常在未指定大小时设置为适合可用设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下CSS类选择器控制查看区域的外观：

```
.s7smartcropvideoviewer 
```

## 主查看器区域的CSS属性 {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>查看器宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>查看器高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有白色背景的智能裁剪视频查看器(#FFFFFF)，并使其大小为512 x 288像素，请执行以下操作：

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
