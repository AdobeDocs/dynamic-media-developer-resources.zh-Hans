---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

交互式视频查看器的配置属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 启用或禁用用户使用鼠标或使用触控手势滚动色板的功能。 </p> </td> 
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
