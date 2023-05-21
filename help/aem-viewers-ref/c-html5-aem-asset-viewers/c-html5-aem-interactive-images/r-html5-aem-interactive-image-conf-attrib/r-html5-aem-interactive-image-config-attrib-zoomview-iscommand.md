---
title: ZoomView.iscommand
description: 套用至縮放影像的「影像伺服」命令字串。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

套用至縮放影像的「影像伺服」命令字串。

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 若在URL中指定，則所有出現的 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 必須為HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在檢視器URL中指定時：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
