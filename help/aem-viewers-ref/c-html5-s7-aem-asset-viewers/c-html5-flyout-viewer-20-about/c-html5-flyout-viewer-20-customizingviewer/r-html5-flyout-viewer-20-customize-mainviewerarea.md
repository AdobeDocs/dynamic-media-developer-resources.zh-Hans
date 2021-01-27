---
description: 主视图区是弹出视图和色板所占用的区域。
seo-description: 主视图区是弹出视图和色板所占用的区域。
seo-title: 主查看器区域
solution: Experience Manager
title: 主查看器区域
topic: Dynamic Media
uuid: bc0beeaf-3e7d-4ede-9a7d-04afb1724e44
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---


# 主查看器区域{#main-viewer-area}

主视图区是弹出视图和色板所占用的区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7flyoutviewer
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

示例——设置具有白色背景(`#FFFFFF`)的弹出查看器，并使其大小为260 x 500像素。

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```

