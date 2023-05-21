---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

无。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

在檢視器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
