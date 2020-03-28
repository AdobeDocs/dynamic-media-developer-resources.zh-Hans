---
description: 辅助控件栏是矩形区域，当在CSS中提供时，该区域包含“第一页”和“最后一页”按钮以及“页面指示符”。
seo-description: 辅助控件栏是矩形区域，当在CSS中提供时，该区域包含“第一页”和“最后一页”按钮以及“页面指示符”。
seo-title: 辅助控制栏
solution: Experience Manager
title: 辅助控制栏
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助控制栏{#secondary-control-bar}

辅助控件栏是矩形区域，当在CSS中提供时，该区域包含“第一页”和“最后一页”按钮以及“页面指示符”。

默认情况下，它仅显示在移动电话上，并位于查看器的底部。 它始终采用整个可用的查看器宽度。 可以通过CSS相对于查看器容器更改其颜色、高度和垂直位置。

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
   <td colname="col2"> <p>从查看器顶部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从查看器底部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控件栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>辅助控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个灰色的辅助控制栏，该控件栏高72像素，位于查看器容器的底部。

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

