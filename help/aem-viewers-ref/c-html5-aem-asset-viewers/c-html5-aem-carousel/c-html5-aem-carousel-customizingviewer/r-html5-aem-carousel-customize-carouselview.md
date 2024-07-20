---
title: 轮播视图
description: 主视图由横幅图像组成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: aa41b209-11c7-4744-aaa5-dc0b503607c6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 1%

---

# 轮播视图{#carousel-view}

主视图由横幅图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 主视图的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```
