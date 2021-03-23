---
description: 主视图区域是缩放图像所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-description: 主视图区域是缩放图像所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。
seo-title: 主查看器区域
solution: Experience Manager
title: 主查看器区域
uuid: f37b8d25-4bd6-481e-88e7-98192186b177
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# 主查看器区域{#main-viewer-area}

主视图区域是缩放图像所占用的区域。 当未指定大小时，它通常设置为适合可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

```
.s7basiczoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置具有白色背景(`#FFFFFF`)的查看器，使其大小为512 x 288像素。

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

