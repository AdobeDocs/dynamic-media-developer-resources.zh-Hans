---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数值|虚线</span> </p> </td> 
   <td colname="col2"> <p> 配置设置指示器的呈现样式。 </p> <p>当设置为点线</span>的<span class="codeph">时，组件会为所有页面呈现相同的指示器。 </span></p> <p>当设置为<span class="codeph">数值</span>时，它会在每个指示器元素中放置一个基于1的页码。 </p> <p>具有触摸输入的设备不支持<span class="codeph">数值</span>操作模式。 该组件而是在此类设备上使用<span class="codeph">虚线</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
