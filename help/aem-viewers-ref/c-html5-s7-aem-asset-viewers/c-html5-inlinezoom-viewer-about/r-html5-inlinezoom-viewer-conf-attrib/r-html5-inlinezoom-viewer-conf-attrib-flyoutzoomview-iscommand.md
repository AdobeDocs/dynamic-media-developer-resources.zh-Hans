---
title: FlyoutZoomView.iscommand
description: FlyoutZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2ae17dc8-2728-4ee5-ba88-45d78a0f4d9a
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>套用至FlyoutZoomView主影像和已放大檢視的「影像伺服」命令字串。 若在URL中指定，請確定您對所有出現的專案進行HTTP編碼 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 作為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> <p> <p>注意：不支援影像大小調整操控命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

无。

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
