---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件從影像伺服器載入影像時，所使用的影像格式。 格式是影像伺服器和使用者端瀏覽器支援的任何值。 </p> <p>如果影像格式結尾為 <span class="codeph"> -alpha</span>，元件會將影像呈現為透明內容。 至於所有其他影像格式值，元件會將影像視為不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
