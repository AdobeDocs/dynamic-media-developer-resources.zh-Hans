---
title: 辅助控制条
description: 辅助控制栏是矩形区域，其中包含在CSS中提供“首页”和“最后一页”按钮以及“页面指示器”。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# 辅助控制条{#secondary-control-bar}

辅助控制栏是矩形区域，其中包含在CSS中提供“首页”和“最后一页”按钮以及“页面指示器”。

默认情况下，该查看器仅在手机上的查看器底部显示。 它始终采用所有可用的查看器宽度。 可以通过CSS相对于查看器容器更改其颜色、高度和垂直位置。

通过以下CSS类选择器控制辅助控制栏的外观：

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
   <td colname="col2"> <p>查看器顶部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>查看器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>辅助控制栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个高度为72像素且位于查看器容器底部的灰色次级控制栏。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
