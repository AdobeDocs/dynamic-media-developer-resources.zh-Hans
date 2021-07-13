---
description: 当当前资产是旋转集时，主视图由旋转图像组成。
solution: Experience Manager
title: 旋转视图
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# 旋转视图{#spin-view}

当当前资产是旋转集时，主视图由旋转图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

通过以下CSS类选择器控制查看区域的外观：

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> 旋转视图的十六进制格式背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使旋转视图透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
