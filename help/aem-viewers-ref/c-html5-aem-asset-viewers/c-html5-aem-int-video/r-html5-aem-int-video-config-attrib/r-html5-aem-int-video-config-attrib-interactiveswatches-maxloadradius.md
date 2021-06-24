---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

交互式视频查看器的配置属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预加载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，在初始化组件或更改资产时，会同时加载所有样本。 </p> <p>当设置为<span class="codeph"> 0</span>时，仅加载可见的色板。 </p> <p>设置为<span class="codeph"><span class="varname"> preloadnbr</span></span>以定义预加载可见区域周围有多少不可见的行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
