---
description: Video360查看器的配置属性。
seo-description: Video360查看器的配置属性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Video360查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 </p> <p> 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，面板将沿指定方向滚出，而不需要额外的边界检查，这可能导致面板被外部容器卡住。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件会首先将基板位置移至SocialShare的底部，并尝试从底部、右侧或左侧从此基本位置展开面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基面板位置移到顶部，并在顶部、右侧和左侧重复滚出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑。 但是，它首先将基向右移动，尝试右、下和上转出方向，然后将基向左移动，尝试左、下和上转出方向。 </p> </td> 
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

