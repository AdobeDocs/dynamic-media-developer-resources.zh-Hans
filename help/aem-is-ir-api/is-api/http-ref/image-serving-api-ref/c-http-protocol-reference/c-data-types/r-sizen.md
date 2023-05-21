---
description: 標準化大小。 用來指定影像大小或矩形大小，以圖層0或其他影像的大小為基準進行標準化。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# sizeN{#sizen}

標準化大小。 用來指定影像大小或矩形大小，以圖層0或其他影像的大小為基準進行標準化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>相對於其他影像的標準化寬度和高度（實數、實數、大於0） </p></td> 
 </tr> 
</table>

兩者 *nx* 和 *ny* 必須大於0。 0,0表示應使用特定的預設大小。 1,1指定等於參考影像的大小。
