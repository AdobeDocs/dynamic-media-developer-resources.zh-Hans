---
description: 指定按钮容器的幻灯片动画方向。
seo-description: 指定按钮容器的幻灯片动画方向。
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按钮容器的幻灯片动画方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 当设置为 <span class="codeph"> 、</span>、向下 <span class="codeph"> 、向左或向右方向时</span><span class="codeph"></span><span class="codeph"></span>，面板在不附加边界检查的情况下向上滚动，这会导致面板被外部容器裁切。 </p> <p>当设置为 <span class="codeph"> 适合垂直时</span>，组件首先将基板位置移至“收藏夹”菜单的底部，并尝试从此基本位置向下列方向之一展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试均失败，则组件会尝试将基板位置移到顶部，并从顶部、右侧和左侧重复滚出尝试。 </p> <p>当设置为 <span class="codeph"> fit-lateral时</span>，组件使用类似的逻辑。 基座首先向右移动，向右、向下和向上展开。 然后，它将底座向左移动，向左、向下和向上展开。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
