---
title: SocialShare.bearing
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

智能裁剪视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 为按钮容器指定幻灯片动画的方向。 </p> <p> 当设置为 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>或 <span class="codeph"> 右</span>时，面板会按指定方向滚出，而不会进行额外的边界检查，这可能导致外部容器剪切面板。 </p> <p>当设置为 <span class="codeph"> 拟垂直</span>，该组件会首先将基础面板位置移至SocialShare的底部，并尝试从这些基础位置从底部、右侧或左侧推出面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，组件会尝试将基板位置移动到顶部，并在顶部、右部和左侧重复尝试转出。 </p> <p>当设置为 <span class="codeph"> 侧向配合</span>，则组件会使用类似的逻辑。 但是，它会先将基本向右移动，尝试右、下和上转出方向，然后将基本向左移动，尝试左、下和上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
