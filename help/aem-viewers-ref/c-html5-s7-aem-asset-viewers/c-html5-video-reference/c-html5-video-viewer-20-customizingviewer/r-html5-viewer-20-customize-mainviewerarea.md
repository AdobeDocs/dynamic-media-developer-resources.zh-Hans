---
description: 主视图区域被视频占用。 当未指定大小时，它通常设置为适合可用的设备屏幕。
solution: Experience Manager
title: 主查看器区域
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '111'
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有白色背景的视频查看器(#FFFFFF)并使其大小为512 x 288像素，请执行以下操作：

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

