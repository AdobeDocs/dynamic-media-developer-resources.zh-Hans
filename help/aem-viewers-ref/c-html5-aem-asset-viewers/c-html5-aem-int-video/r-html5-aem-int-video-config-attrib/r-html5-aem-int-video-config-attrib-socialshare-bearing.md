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
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

交互式视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 为按钮容器指定幻灯片动画的方向。 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，该面板将按指定方向滚出，而无需进行任何额外的范围检查，这可能导致该面板被外部容器剪切。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件会首先将基板位置移至SocialShare的底部。 然后，它尝试从此基位置沿下列方向之一展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，组件会尝试将基面板位置移到顶部，并重复从顶部、右侧和左侧转出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但首先将基本移至右侧，然后右键、向下和向上转出方向。 然后，它将基座向左移动，尝试左、下和上移方向。 </p> </td> 
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
