---
description: 主视图区域是目录图像所占用的区域。 通常，当未指定大小时，它会设置为适合可用的设备屏幕。
seo-description: 主视图区域是目录图像所占用的区域。 通常，当未指定大小时，它会设置为适合可用的设备屏幕。
seo-title: 主查看器区域
solution: Experience Manager
title: 主查看器区域
topic: Dynamic media
uuid: 2ad21319-7a0e-44fd-8866-3055e8ff8913
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 主查看器区域{#main-viewer-area}

主视图区域是目录图像所占用的区域。 通常，当未指定大小时，它会设置为适合可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

```
.s7ecatalogsearchviewer
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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置具有白色背景( `#FFFFFF`)的查看器，并使其大小为512 x 288像素。

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

