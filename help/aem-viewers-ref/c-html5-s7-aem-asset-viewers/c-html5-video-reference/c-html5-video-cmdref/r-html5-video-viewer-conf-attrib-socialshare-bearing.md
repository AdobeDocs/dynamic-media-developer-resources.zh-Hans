---
title: SocialShare.bearing
description: Video Viewer的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Video Viewer的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|适合 — 垂直|适合 — 横向</span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画的方向。 </p> <p> 当设置为 <span class="codeph"> 向上</span>， <span class="codeph"> 下</span>， <span class="codeph"> left</span>，或 <span class="codeph"> 右</span>时，面板会以指定方向滚出，而不会进行额外的边界检查，这可能会导致面板被外部容器剪切。 </p> <p>当设置为 <span class="codeph"> 垂直适合</span>，组件首先将基础面板位置移到SocialShare的底部，并尝试从此类基础位置从底部、右侧或左侧转出面板。 在每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并在顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为 <span class="codeph"> 拟合横向</span>，组件使用类似的逻辑。 但是，它会先将基面移动到右侧，尝试右、下和上转出方向，然后将基面移动到左侧，尝试左、下和上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
