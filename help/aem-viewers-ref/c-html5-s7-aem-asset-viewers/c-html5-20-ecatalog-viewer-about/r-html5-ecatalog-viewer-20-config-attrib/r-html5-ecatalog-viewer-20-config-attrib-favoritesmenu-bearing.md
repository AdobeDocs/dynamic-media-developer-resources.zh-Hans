---
title: FavoritesMenu.bearing
description: 指定按鈕容器的幻燈片動畫方向。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

指定按鈕容器的幻燈片動畫方向。

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 向上|向下|向左|向右|垂直適合|橫向適合</span> </p> </td> 
   <td colname="col2"> <p> 當設定為 <span class="codeph"> 向上</span>， <span class="codeph"> 向下</span>， <span class="codeph"> left</span>，或 <span class="codeph"> 右側</span>，面板會以指定方向轉出，而不會進行額外的邊界檢查，而這會造成面板被外部容器剪裁。 </p> <p>當設定為 <span class="codeph"> 垂直符合</span>，元件會先將基礎面板位置移至「我的最愛」功能表的底部。 它會嘗試從此類基本位置以下列方向之一轉出面板：下、右、左。 每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂部，並從頂部、右側和左側重複轉出嘗試。 </p> <p>當設定為 <span class="codeph"> 適合 — 橫向</span>，元件會使用類似的邏輯。 基底會先向右移動，嘗試向右、向下和向上轉出方向。 然後，它會將基底向左移動，嘗試向左、向下和向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
