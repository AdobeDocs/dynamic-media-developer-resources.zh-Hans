---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,Business Practitioner
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数值|虚线</span> </p> </td> 
   <td colname="col2"> <p> 配置设置指示器的呈现样式。 </p> <p>当设置为<span class="codeph">虚线</span>时，组件会为所有页面呈现相同的指示器。 </p> <p>当设置为<span class="codeph">数值</span>时，它会在每个指示器元素中放置一个基于1的页码。 </p> <p>能够触摸输入的设备不支持<span class="codeph">数值</span>操作模式。 该组件而是在此类设备上使用<span class="codeph">虚线</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
