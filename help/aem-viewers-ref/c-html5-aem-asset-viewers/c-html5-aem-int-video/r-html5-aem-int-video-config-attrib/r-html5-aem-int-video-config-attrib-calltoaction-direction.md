---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
topic: Dynamic media
uuid: fe182e8f-696d-4515-afdb-49964a374dae
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.direction{#calltoaction-direction}

交互式视频查看器的配置属性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> 指定缩览图填充视图的方式。 </p> <p>设置为 <span class="codeph"> 左 </span> 侧可设置从左到右的填充顺序。 </p> <p>设置为 <span class="codeph"> 右 </span> 侧可颠倒顺序，以便视图按从右到左、从上到下的方向填充。 </p> <p>设置为 <span class="codeph"> 自动 </span> ，当区域设置设置为“ja”时，组件应用正确 <span class="codeph"> 的模式 </span>;否则， <span class="codeph"> 将使 </span> 用左边。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

