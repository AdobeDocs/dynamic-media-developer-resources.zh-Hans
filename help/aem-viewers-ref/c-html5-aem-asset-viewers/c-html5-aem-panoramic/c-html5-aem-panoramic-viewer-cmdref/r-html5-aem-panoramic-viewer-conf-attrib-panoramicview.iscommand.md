---
title: PanoramicView.iscommand
description: 全景檢視器的組態屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

全景檢視器的組態屬性。

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 套用至影像的「影像伺服」命令字串。  若在URL中指定，請確定您對所有出現的專案進行HTTP編碼 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 作為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

無預設值。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在檢視器URL中指定時。

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

在設定資料中指定時。

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
