---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: Developer,Business Practitioner
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定组件预加载行为。 当设置为<span class="codeph"> -1</span>时，在初始化组件或更改资产时，会同时加载所有样本。 </p> <p>当设置为<span class="codeph"> 0</span>时，仅加载可见的色板。 </p> <p><span class="codeph"><span class="varname"> </span></span> preloadnbr定义预加载可见区域周围的不可见行/列数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`
