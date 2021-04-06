---
description: 主视图由静态图像组成。
solution: Experience Manager
title: 缩放视图
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: 开发人员，商业从业者
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---

# 缩放视图{#zoom-view}

主视图由静态图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

```
.s7interactiveimage .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 主视图的十六进制格式背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
