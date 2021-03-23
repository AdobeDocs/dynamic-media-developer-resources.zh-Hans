---
description: Swatches.align
solution: Experience Manager
title: Swatches.align
uuid: 5cff285b-69f0-4ffe-b165-c2d1fdc8aa75
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

指定组件区域内色板容器的内部对齐（锚定）。 在“色板”中，内部缩览图容器会被调整为大小，因此只显示整数色板。 因此，内部容器和外部组件边界之间存在一些填充。 此命令指定内部色板容器在组件内的放置方式。

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> 设置水平色板的对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> 设置垂直色板的对齐方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`center,center`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
