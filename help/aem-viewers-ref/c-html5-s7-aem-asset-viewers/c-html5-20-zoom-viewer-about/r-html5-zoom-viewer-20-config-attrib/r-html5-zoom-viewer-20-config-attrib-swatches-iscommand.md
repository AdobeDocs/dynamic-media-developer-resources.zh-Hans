---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: e375f3ec-82f3-441d-9e01-d0ea5605bd25
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 套用至所有色票的「影像伺服」命令字串。 若在URL中指定，請確定您對所有出現的專案進行HTTP編碼 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 作為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> <p> <p>注意：不支援影像大小調整操控命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在檢視器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
