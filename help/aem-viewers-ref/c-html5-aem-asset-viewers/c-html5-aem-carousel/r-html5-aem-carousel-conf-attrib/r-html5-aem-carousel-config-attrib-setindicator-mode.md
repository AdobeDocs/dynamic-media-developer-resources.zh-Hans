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
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数值|点线</span> </p> </td> 
   <td colname="col2"> <p> 配置设置指示器的渲染样式。 </p> <p>当设置为 <span class="codeph"> 虚线 </span>时，组件呈现所有页面的相同指示器。 </p> <p>当设置为 <span class="codeph"> 数值</span> 它在每个指标元素内放置一个从1开始的页码。 </p> <p>此 <span class="codeph"> 数值</span> 具有触摸输入的设备不支持操作模式。 相反，组件使用 <span class="codeph"> 虚线</span> 在此类设备上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
