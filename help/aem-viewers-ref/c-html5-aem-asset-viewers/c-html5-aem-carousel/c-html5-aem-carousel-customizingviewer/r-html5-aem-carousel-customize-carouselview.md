---
description: 主视图由横幅图像组成。
seo-description: 主视图由横幅图像组成。
seo-title: 旋转式视图
solution: Experience Manager
title: 旋转式视图
topic: Dynamic Media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---


# 传送视图{#carousel-view}

主视图由横幅图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7carouselviewer .s7carouselview
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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 主视图的十六进制格式背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主视图透明。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

