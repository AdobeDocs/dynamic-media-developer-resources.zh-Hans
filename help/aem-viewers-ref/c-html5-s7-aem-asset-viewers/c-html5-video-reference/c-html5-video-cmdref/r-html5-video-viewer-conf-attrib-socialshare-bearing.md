---
title: SocialShare.bearing
description: 視訊檢視器的設定屬性。
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

視訊檢視器的設定屬性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 向上|向下|向左|向右|垂直適合|橫向適合</span> </p> </td> 
   <td colname="col2"> <p> 指定按鈕容器的幻燈片動畫方向。 </p> <p> 當設定為 <span class="codeph"> 向上</span>， <span class="codeph"> 向下</span>， <span class="codeph"> left</span>，或 <span class="codeph"> 右側</span>，面板會以指定方向轉出，而不會進行額外的邊界檢查，這會導致面板被外部容器剪裁。 </p> <p>當設定為 <span class="codeph"> 垂直符合</span>，元件會先將基礎面板位置移至SocialShare的底部，並嘗試從此類基礎位置從底部、右側或左側轉出面板。 每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂部，並在頂部、右側和左側重複轉出嘗試。 </p> <p>當設定為 <span class="codeph"> 適合 — 橫向</span>，元件會使用類似的邏輯。 但是，它會先將基底向右移動，嘗試向右、向下和向上轉出方向，然後將基底向左移動，嘗試向左、向下和向上轉出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
