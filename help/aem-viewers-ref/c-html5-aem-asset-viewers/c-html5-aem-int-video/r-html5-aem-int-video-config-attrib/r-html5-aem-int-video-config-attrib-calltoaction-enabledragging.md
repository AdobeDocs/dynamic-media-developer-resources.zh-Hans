---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

交互式视频查看器的配置属性。

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 启用或禁用用户使用鼠标或触控手势滚动缩览图的功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> 在<span class="codeph"> 0-1 </span>范围内，它是实际速度向错误方向移动的百分比值。 </p> <p>如果设置为<span class="codeph"> 1 </span>，则它随鼠标移动。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则不允许您向错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
