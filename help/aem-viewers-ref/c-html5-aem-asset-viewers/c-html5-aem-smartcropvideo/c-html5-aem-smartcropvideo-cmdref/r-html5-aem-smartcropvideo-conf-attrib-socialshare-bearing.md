---
title: SocialShare.bearing
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
TQID: 'https://experienceleague.adobe.com/5b7-Ofn9ZcJTxG-RSwXCbW0pb5EgItA15pG9i2iXUU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

智能裁剪视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">向上|向下|向左|向右|适合 — 垂直|适合 — 横向</span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画的方向。 </p> <p> 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，面板将按指定方向转出，而不进行额外的边界检查，这可能导致面板被外部容器剪切。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基础面板位置移到SocialShare的底部，并尝试从此类基础位置从底部、右侧或左侧推出面板。 每次尝试时，组件都会检查面板是否被外部容器裁剪。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并在顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑。 但是，它首先向右移动基座，尝试向右、向下和向上转出方向，然后向左移动基座，尝试向左、向下和向上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
