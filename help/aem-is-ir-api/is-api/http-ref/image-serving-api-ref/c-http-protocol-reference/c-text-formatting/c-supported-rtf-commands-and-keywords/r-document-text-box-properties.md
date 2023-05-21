---
description: 文字方塊支援下列檔案屬性。
solution: Experience Manager
title: 檔案（文字方塊）屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---

# 檔案（文字方塊）屬性{#document-text-box-properties}

文字方塊支援下列檔案屬性。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>字型表格。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>字型的字元集 <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGB色彩表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK色彩表。 </p> </td> 
   <td> <p>Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>「影像伺服」色彩的色彩表。 </p> </td> 
   <td> <p>Dynamic Media擴充功能； <span class="codeph"> textPs= </span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>紅色元件。 </p> </td> 
   <td> <p>只能出現在 <span class="codeph"> \colortbl </span>； 0至255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \綠色 <span class="varname"> N </span> </span> </td> 
   <td> <p>綠色元件。 </p> </td> 
   <td> <p>只能出現在 <span class="codeph"> \colortbl </span>； 0至255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \藍色 <span class="varname"> N </span> </span> </td> 
   <td> <p>藍色元件。 </p> </td> 
   <td> <p>只能出現在 <span class="codeph"> \colortbl </span>； 0至255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \青色 <span class="varname"> N </span> </span> </td> 
   <td> <p>青色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在 <span class="codeph"> \cmykcolortbl </span>； 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \洋紅色 <span class="varname"> N </span> </span> </td> 
   <td> <p>洋紅色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在 <span class="codeph"> \cmykcolortbl </span>； 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黃色 <span class="varname"> N </span> </span> </td> 
   <td> <p>黃色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在 <span class="codeph"> \cmykcolortbl </span>； 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>黑色顏色元件。 </p> </td> 
   <td> <p>Dynamic Media擴充功能；只能出現在 <span class="codeph"> \cmykcolortbl </span>； 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>左邊界。 </p> </td> 
   <td> <p>崔普； <span class="codeph"> textPs= </span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>右邊界。 </p> </td> 
   <td> <p>崔普； <span class="codeph"> textPs= </span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>上邊界。 </p> </td> 
   <td> <p>崔普； <span class="codeph"> textPs= </span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>下方邊界。 </p> </td> 
   <td> <p>崔普； <span class="codeph"> textPs= </span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>文字方塊中的文字靠上對齊。 </p> </td> 
   <td> <p>默认 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>文字方塊中的靠下對齊文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>文字方塊中的文字置中對齊。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>文字流程方向。 </p> </td> 
   <td> <p>特定語言的文字流程； <span class="codeph"> textPs= </span> 僅0 （預設）左至右、上至下（歐洲） 1上至下、右至左（遠東） </p> </td> 
  </tr> 
 </tbody> 
</table>
