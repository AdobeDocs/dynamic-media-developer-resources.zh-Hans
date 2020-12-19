---
description: 主视图区域是缩放图像和色板所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-description: 主视图区域是缩放图像和色板所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-title: 主查看器区域
solution: Experience Manager
title: 主查看器区域
topic: Dynamic media
uuid: 689116cb-bbb9-4e26-9c16-9229330c4034
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---


# 主查看器区域{#main-viewer-area}

主视图区域是缩放图像和色板所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

在嵌入模式下工作（当主查看器区域具有明确大小时）时，查看器会按处理单个图像的色板组件的高度自动减小其主区域的高度，因此不需要色板。

**主查看器区域的CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>查看器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>查看器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置具有白色背景(`#FFFFFF`)的查看器，并使其大小为512 x 288像素。

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

