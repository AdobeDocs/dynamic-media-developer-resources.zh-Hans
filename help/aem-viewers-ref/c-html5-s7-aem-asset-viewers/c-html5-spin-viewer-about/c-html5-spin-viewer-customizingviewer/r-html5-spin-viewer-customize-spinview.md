---
description: 主视图由旋转图像组成。
solution: Experience Manager
title: 旋转视图
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: Developer,Business Practitioner
exl-id: d3274fe3-1a47-448e-acc6-6df77c6a4211
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# 旋转视图{#spin-view}

主视图由旋转图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

通过以下CSS类选择器控制查看区域的外观：

```
.s7spinviewer .s7spinview
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
   <td colname="col2"> <p> 主视图以十六进制格式显示的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```
