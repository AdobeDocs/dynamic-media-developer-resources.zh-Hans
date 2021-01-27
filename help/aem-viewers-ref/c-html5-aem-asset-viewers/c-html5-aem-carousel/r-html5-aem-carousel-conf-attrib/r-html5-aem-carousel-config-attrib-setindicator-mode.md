---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
topic: Dynamic Media
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数字|虚点</span> </p> </td> 
   <td colname="col2"> <p> 配置设置指示符的呈现样式。 </p> <p>如果设置为<span class="codeph"> dotted</span>，则组件会为所有页面呈现相同的指示符。 </p> <p>当设置为<span class="codeph">数字</span>时，它将基于1的页码放在每个指示符元素中。 </p> <p>能够触摸输入的设备不支持<span class="codeph">数字</span>操作模式。 而是在此类设备上使用<span class="codeph"> dotted</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
