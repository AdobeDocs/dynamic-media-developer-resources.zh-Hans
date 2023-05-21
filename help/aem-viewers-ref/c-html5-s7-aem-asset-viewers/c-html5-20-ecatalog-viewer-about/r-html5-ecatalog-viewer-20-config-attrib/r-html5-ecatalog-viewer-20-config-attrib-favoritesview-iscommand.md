---
title: FavoritesView.iscommand
description: 套用至所有縮圖的「影像伺服」命令字串。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

套用至所有縮圖的「影像伺服」命令字串。

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 若在URL中指定，則所有出現的 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 必須為HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在檢視器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
