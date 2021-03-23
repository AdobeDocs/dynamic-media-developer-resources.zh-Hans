---
description: 当当前资产是旋转集时，主视图由旋转图像组成。
seo-description: 当当前资产是旋转集时，主视图由旋转图像组成。
seo-title: 旋转视图
solution: Experience Manager
title: 旋转视图
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# 旋转视图{#spin-view}

当当前资产是旋转集时，主视图由旋转图像组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 旋转视图的十六进制格式背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使旋转视图透明。

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

