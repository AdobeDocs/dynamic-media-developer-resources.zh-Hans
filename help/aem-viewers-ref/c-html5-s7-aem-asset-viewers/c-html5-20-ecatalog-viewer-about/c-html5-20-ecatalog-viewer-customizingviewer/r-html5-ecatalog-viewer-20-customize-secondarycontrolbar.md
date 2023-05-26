---
title: 辅助控制栏
description: 辅助控制栏是包含“第一页”和“最后一页”按钮以及在CSS中可用的页面指示器的矩形区域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# 辅助控制栏{#secondary-control-bar}

辅助控制栏是包含“第一页”和“最后一页”按钮以及在CSS中可用的页面指示器的矩形区域。

默认情况下，它仅在手机上显示，并位于查看器底部。 它始终采用所有可用的查看器宽度。 可以通过CSS更改其相对于查看器容器的颜色、高度和垂直位置。

辅助控件栏的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

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
   <td colname="col2"> <p>从查看器顶部开始定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从查看器底部开始定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>辅助控制栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个高度为72像素且位于查看器容器底部的灰色辅助控制栏。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
