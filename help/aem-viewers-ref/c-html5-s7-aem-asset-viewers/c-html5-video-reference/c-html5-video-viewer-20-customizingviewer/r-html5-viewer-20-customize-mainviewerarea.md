---
description: 主视图区域被视频占用。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-description: 主视图区域被视频占用。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-title: 主查看器区域
solution: Experience Manager
title: 主查看器区域
topic: Dynamic Media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---


# 主查看器区域{#main-viewer-area}

主视图区域被视频占用。 当未指定大小时，它通常设置为适合可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

以下CSS类选择器控制查看区域的外观：

```
.s7videoviewer 
```

## 主查看器区域{#css-properties-of-the-main-viewer-area}的CSS属性

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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有白色背景(#FFFFFF)的视频查看器并使其大小为512 x 288像素，请执行以下操作：

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

