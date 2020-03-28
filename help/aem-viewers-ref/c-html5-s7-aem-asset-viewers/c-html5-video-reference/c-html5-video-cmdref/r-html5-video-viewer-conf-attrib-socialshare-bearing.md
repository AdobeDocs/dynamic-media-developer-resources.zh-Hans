---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: SocialShare.bearding
solution: Experience Manager
title: SocialShare.bearding
topic: Dynamic media
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.bearding{#socialshare-bearing}

视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 为按钮容器指定幻灯片动画的方向。 </p> <p> 当设置为 <span class="codeph"> 、</span>、向下 <span class="codeph"> 、向左或向右</span><span class="codeph"></span><span class="codeph"></span>，面板在指定方向上向上滚出，而没有额外的边界检查，这会导致面板被外部容器剪切。 </p> <p>当设置为 <span class="codeph"> 适合垂直时</span>，组件首先将基板位置移至SocialShare的底部，并尝试从底部、右侧或左侧从此基本位置展开面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试均失败，则组件会尝试将基板位置移到顶部，并在顶部、右侧和左侧重复滚出尝试。 </p> <p>当设置为 <span class="codeph"> fit-lateral时</span>，组件使用类似的逻辑。 但是，它首先将基向右移动，尝试右、下和上转出方向，然后将基向左移动，尝试左、下和上转出方向。 </p> </td> 
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

