---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数值|虚点</span> </p> </td> 
   <td colname="col2"> <p> 配置设置指示符的呈现样式。 </p> <p>设置为<span class="codeph"> dotted</span>时，组件会为所有页面呈现相同的指示器。 </p> <p>当设置为<span class="codeph"> numeric</span>时，它将基于1的页码放在每个指示符元素中。 </p> <p>能够触摸输入的设备不支持<span class="codeph">数字</span>操作模式。 相反，该组件在此类设备上使用<span class="codeph"> dotted</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
