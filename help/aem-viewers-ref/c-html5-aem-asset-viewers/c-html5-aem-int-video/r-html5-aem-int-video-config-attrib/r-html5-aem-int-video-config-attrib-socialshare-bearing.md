---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

交互式视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 为按钮容器指定幻灯片动画的方向。 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，该面板将按指定方向滚出，而无需进行任何额外的范围检查，这可能导致该面板被外部容器剪切。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基板位置移至SocialShare的底部，并尝试从此基位置沿以下任一方向展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，组件会尝试将基板位置移动到顶部，并从顶部、右侧和左侧重复推出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但首先将基本移至右侧，然后右键、下键和上键转出方向。 然后，它将基座向左移动，尝试左、下和上移方向。 </p> </td> 
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
