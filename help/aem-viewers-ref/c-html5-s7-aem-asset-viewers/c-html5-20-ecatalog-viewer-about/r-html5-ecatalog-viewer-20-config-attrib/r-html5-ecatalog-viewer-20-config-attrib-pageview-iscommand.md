---
title: PageView.iscommand
description: PageView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d1b05fe7-901b-4030-9b71-e4e0e5191abf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 套用至頁面影像的「影像伺服」命令字串。 若在URL中指定，則所有出現的 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 必須為HTTP編碼為 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>（分別）。 </p> <p> <p>注意：不支援影像大小調整操控命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-df5a0604766b4ac2b9a6742b377e427c}

可选.

## 默认 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

无。

## 示例 {#section-813de2905d6c44c0991cfe0931581462}

在檢視器URL中指定時。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在設定資料中指定時。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
