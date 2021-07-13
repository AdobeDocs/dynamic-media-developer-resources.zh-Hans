---
description: 主视图区域是缩放图像所占用的区域。 通常在未指定任何大小时将其设置为适合可用设备屏幕。
solution: Experience Manager
title: 主查看器区域
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,User
exl-id: c8005e7e-dff6-4f40-a94c-6fb6640e827f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# 主查看器区域{#main-viewer-area}

主视图区域是缩放图像所占用的区域。 通常在未指定任何大小时将其设置为适合可用设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

通过以下CSS类选择器控制查看区域的外观：

```
.s7interactiveimage
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
   <td colname="col2"> <p> 以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置具有白色背景的查看器(`#FFFFFF`)，并使其大小为1174 x 500像素。

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
