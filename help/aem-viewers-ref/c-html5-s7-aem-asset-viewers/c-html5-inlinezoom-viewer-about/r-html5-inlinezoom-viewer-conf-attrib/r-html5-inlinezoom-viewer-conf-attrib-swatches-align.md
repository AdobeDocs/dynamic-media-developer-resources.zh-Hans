---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: d9db34f3-66df-45c2-9727-bdcdf09773db
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

指定组件区域内色板容器的内部对齐（锚定）。 在“色板”中，内部缩略图容器的大小是大小，因此只显示整数色板。 因此，内部容器与外部组件范围之间存在一些内边距。 此命令指定内部色板容器在组件中的放置方式。

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 左|中|右</span> </p> </td> 
   <td colname="col2"> <p> 设置水平色板对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 顶部|中心|底部</span> </p> </td> 
   <td colname="col2"> <p> 设置垂直色板对齐方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`center,center`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`align=left,top`
