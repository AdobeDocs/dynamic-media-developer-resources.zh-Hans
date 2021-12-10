---
title: FavoritesMenu.bearing
description: 指定按钮容器的幻灯片动画方向。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按钮容器的幻灯片动画方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 当设置为 <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>或 <span class="codeph"> 右</span>时，面板会沿指定方向滚出，而不会进行额外的边界检查，这会导致外部容器剪切面板。 </p> <p>当设置为 <span class="codeph"> 拟垂直</span>，组件会首先将基面板位置移至“收藏夹”菜单的底部。 它会尝试从此基位置沿下列方向之一展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，组件会尝试将基板位置切换到顶部，并从顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为 <span class="codeph"> 侧向配合</span>，则组件会使用类似的逻辑。 基座首先向右移动，向右、向下和向上展开。 然后，它把底座向左移动，试着左、下、上展开方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
