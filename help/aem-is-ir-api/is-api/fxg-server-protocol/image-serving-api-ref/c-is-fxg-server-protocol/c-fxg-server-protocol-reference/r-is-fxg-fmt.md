---
description: 回應影像格式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# fmt{#fmt}

回應影像格式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 格式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 指定傳送至使用者端之影像資料的影像編碼格式，以及HTTP回覆標頭的對應回應MIME型別。 </p> <p> <span class="codeph">  jpeg </span>：有損JPEG </p> <p> <span class="codeph"> png </span>：無損失PNG </p> <p> <span class="codeph"> png-alpha </span>：使用Alpha色版的無損失PNG </p> <p> <span class="codeph">  tif </span>：TIFF </p> <p> <span class="codeph"> tif-alpha </span>：使用Alpha色版進行TIFF </p> <p> <span class="codeph">  swf </span>：內嵌於Adobeswf檔案中的有損JPEG </p> <p> <span class="codeph"> pdf </span>：內嵌於PDF中的影像 </p> <p> <span class="codeph"> gif </span>：使用2到256色的GIF </p> <p> <span class="codeph"> gif-alpha </span>：GIF具有2到255種色彩加上關鍵色彩透明度 </p> <p> <span class="codeph"> fxg </span>：套用變數和DOM操作的FXG </p> <p> <span class="codeph">  fxgraw </span>：原始FXG儲存在伺服器上 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixeltype</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb |灰色 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 可用於影響輸出色域。 </p> <p> <span class="codeph">  rgb </span>：傳回RGB影像資料 </p> <p> <span class="codeph"> 灰色 </span>：傳回灰階影像資料 </p> <p> <span class="codeph"> cmyk </span>：傳回CMYK影像資料 </p> </td> 
 </tr> 
</table>

`tiffCompression` 只有在tif、tif-alpha指定為格式時才允許使用。 如需這些影像格式支援的壓縮選項，請參閱下表。

`qlt=` 可用於設定下列格式的JPEG編碼選項：JPEG、具有JPEG壓縮的TIFF。 quantize=可用於fmt=gif或fmt=gif-alpha。 如需詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

所有格式都會傳回8位元/畫素元件，而且 `pixelTypes[7]`.

下表列出格式與檔案的有效組合： `pixelType`，則為對應的HTTP回應MIME型別。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 格式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixeltype</span> </p> </th> 
   <th colname="col3" class="entry"> <p>回應MIME型別 </p> </th> 
   <th colname="col4" class="entry"> <p>內嵌ICC設定檔 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb、灰色、cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png， png-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif， tif-alpha </p> </td> 
   <td> <p>rgb、灰色、cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> (無 | lzw | zip | jpeg)，qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf， swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb、灰色、cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif， gif-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
