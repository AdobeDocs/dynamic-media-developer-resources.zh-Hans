---
description: 主视图由横幅图像组成。
seo-description: 主视图由横幅图像组成。
seo-title: 传送视图
solution: Experience Manager
title: 传送视图
topic: Dynamic media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 传送视图{#carousel-view}

主视图由横幅图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 以主视图的十六进制格式显示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主视图透明。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

