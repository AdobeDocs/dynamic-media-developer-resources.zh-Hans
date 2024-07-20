---
description: 指定按钮容器的幻灯片动画方向。
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按钮容器的幻灯片动画方向。

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">向上|向下|向左|向右|适合 — 垂直|适合 — 横向</span> </p> </td> 
   <td colname="col2"> <p> 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，面板将按指定方向转出，而不进行额外的边界检查，这会导致面板被外部容器剪切。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基础面板位置移到“收藏夹”菜单的底部，并尝试按以下方向之一从此类基础位置转出面板：底部、右侧、左侧。 在每次尝试时，组件都会检查面板是否被外部容器裁剪。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并从顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑。 基座首先向右移动，尝试向右、向下和向上转出方向。 然后，它向左移动基座，尝试向左、向下和向上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
