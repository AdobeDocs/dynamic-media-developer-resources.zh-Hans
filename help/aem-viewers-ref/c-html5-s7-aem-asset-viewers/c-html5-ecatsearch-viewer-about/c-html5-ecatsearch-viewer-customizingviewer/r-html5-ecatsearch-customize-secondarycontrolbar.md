---
description: 辅助控制栏是矩形区域，当在CSS中可用时，该区域包含“首页”和“末页”按钮以及“页面指示符”。
seo-description: 辅助控制栏是矩形区域，当在CSS中可用时，该区域包含“首页”和“末页”按钮以及“页面指示符”。
seo-title: 辅助控制栏
solution: Experience Manager
title: 辅助控制栏
uuid: 38217d2a-8668-46e1-9df1-f29c1c7e0798
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# 辅助控制栏{#secondary-control-bar}

辅助控制栏是矩形区域，当在CSS中可用时，该区域包含“首页”和“末页”按钮以及“页面指示符”。

默认情况下，它仅显示在移动电话上，并位于查看器底部。 它始终采用整个可用查看器宽度。 可以通过CSS更改其颜色、高度和垂直位置(相对于查看器容器)。

辅助控制栏的外观由以下CSS类选择器控制：

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从查看器顶部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从查看器底部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>辅助控件条的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个高72像素且位于查看器容器底部的灰色辅助控制栏。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

