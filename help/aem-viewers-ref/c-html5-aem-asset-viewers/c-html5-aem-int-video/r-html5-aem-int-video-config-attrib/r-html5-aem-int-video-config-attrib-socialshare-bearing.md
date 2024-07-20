---
title: SocialShare.bearing
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

交互式视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">向上|向下|向左|向右|适合 — 垂直|适合 — 横向</span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，面板将按指定的方向转出，而不执行任何其他边界检查，这可能导致面板被外部容器剪切。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基础面板位置移到SocialShare的底部。 然后，它会尝试从此类基本位置按以下方向之一转出面板：底部、右侧、左侧。 在每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并从顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但先将基数向右移动，然后尝试向右、向下和向上转出方向。 然后，它将底部向左移动，尝试向左、向下和向上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
