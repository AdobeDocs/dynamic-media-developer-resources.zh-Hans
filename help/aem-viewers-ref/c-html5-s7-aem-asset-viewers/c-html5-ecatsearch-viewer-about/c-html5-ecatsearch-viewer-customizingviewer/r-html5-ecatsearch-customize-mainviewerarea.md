---
title: 主查看器区域
description: 主视图区域是目录图像所占用的区域。 它通常设置为在没有指定大小时适应可用的设备屏幕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 854f5fa7-f46d-4c4f-9a44-886fec93f606
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 主查看器区域{#main-viewer-area}

主视图区域是目录图像所占用的区域。 它通常设置为在没有指定大小时适应可用的设备屏幕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

查看区域的外观由以下CSS类选择器控制：

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
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>查看器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>查看器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置具有白色背景(`#FFFFFF`)的查看器，并使其大小为512 x 288像素。

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
