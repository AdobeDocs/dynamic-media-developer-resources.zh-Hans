---
description: 指定按鈕容器的幻燈片動畫方向。
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

指定按鈕容器的幻燈片動畫方向。

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 向上|向下|向左|向右|垂直適合|橫向適合</span> </p> </td> 
   <td colname="col2"> <p> 當設定為 <span class="codeph"> 向上</span>， <span class="codeph"> 向下</span>， <span class="codeph"> left</span>，或 <span class="codeph"> 右側</span>，面板會以指定方向轉出，而不會進行額外的邊界檢查，而這會造成面板被外部容器剪裁。 </p> <p>當設定為 <span class="codeph"> 垂直符合</span>，元件會先將基礎面板位置移至「我的最愛」選單底部，並嘗試從此類基礎位置以下列方向之一轉出面板：底部、右側、左側。 每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂部，並從頂部、右側和左側重複轉出嘗試。 </p> <p>當設定為 <span class="codeph"> 適合 — 橫向</span>，元件會使用類似的邏輯。 基底會先向右移動，嘗試向右、向下和向上轉出方向。 然後，它會將基底向左移動，嘗試向左、向下和向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
