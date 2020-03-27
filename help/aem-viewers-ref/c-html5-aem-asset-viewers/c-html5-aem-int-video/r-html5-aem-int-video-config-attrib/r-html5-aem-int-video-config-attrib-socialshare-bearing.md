---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: SocialShare.bearding
solution: Experience Manager
title: SocialShare.bearding
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.bearding{#socialshare-bearing}

交互式视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 为按钮容器指定幻灯片动画的方向。 当设置为 <span class="codeph"> 、</span>、向下、向左 <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>、或向右指定方向时，面板向上滚出，而不进行任何附加的边界检查，这可能导致面板被外部容器剪切。 </p> <p>当设置为 <span class="codeph"> 适合垂直时</span>，组件首先将基板位置移至SocialShare的底部，并尝试从此基本位置沿以下任一方向展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试均失败，则组件会尝试将基板位置移到顶部，并重复从顶部、右侧和左侧进行的滚出尝试。 </p> <p>当设置为 <span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但首先将基本向右移动，然后向右、向下和向上转出方向。 然后，它将基向左移动，尝试左、下和上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

