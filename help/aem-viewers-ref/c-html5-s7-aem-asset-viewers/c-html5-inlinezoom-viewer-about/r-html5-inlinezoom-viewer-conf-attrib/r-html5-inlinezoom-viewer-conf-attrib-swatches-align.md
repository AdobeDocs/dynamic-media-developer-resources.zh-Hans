---
description: Swatches.align
solution: Experience Manager
title: Swatches.align
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

指定组件区域内色板容器的内部对齐（锚定）。 在“色板”中，内部缩览图容器会被调整为大小，因此只显示整数色板。 因此，内部容器和外部组件边界之间存在一些填充。 此命令指定内部色板容器在组件内的放置方式。

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> 设置水平色板对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
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
