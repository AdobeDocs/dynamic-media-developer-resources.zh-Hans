---
title: fmt
description: 回覆影像格式。 指定傳送至使用者端之影像資料的影像編碼格式，以及HTTP回應標頭的對應回應MIME型別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 4%

---

# fmt {#fmt}

回覆影像格式。 指定傳送至使用者端之影像資料的影像編碼格式，以及HTTP回應標頭的對應回應MIME型別。

` fmt= *`格式`*[,[ *`pixeltype`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 格式 </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>有損JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>有損JPG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>無遺失的PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>使用Alpha色版的無損失PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>使用Alpha色版進行TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>內嵌於Macromedia swf檔的有損JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>有損JPEG與內嵌於Macromedia swf檔案中的deflate-compressed遮色片。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>內嵌在PDF中的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>未壓縮的二進位封裝PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色GIF，加上按鍵色彩透明度。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixeltype </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>傳回RGB影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>灰色 </p> </td> 
  <td class="stentry"> <p>傳回灰階影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>傳回CMYK影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>无 </p> </td> 
  <td class="stentry"> <p>未壓縮。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW (Lempel-Ziv-Welch)壓縮（不失真）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>"Deflate"壓縮（不失真）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG壓縮（失真）。 </p> </td> 
 </tr> 
</table>

*`pixelType`* 效果輸出色域轉換： `icc=` 未指定；預設色彩設定檔對應至 *`pixelType`* 「 」已套用。 如果停用色彩管理，則會套用天真的轉換。 *`pixelType`* 忽略時機 `icc=` 指定，這會決定輸出畫素型別。

*`compression`* 只有在指定tif、tif-alpha或PDF為時才允許 *`format`*. 如需這些影像格式支援的壓縮選項，請參閱下表。

`qlt-` 設定下列格式的JPEG編碼選項：JPEG、使用JPEG壓縮的TIFF、使用JPEG壓縮的PDF以及SWF檔案。 使用 `quantize=` 如果 `fmt=gif` 或 `fmt=gif-alpha`. 如需詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

所有格式和畫素型別都會傳回每個畫素元件8位元。

下表列出下列有效組合： *`format`* 和 *`pixelType`*，對應的HTTP回應MIME型別，是否可以內嵌ICC設定檔(請參閱 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f))，以及可以套用哪些格式特定選項命令。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 格式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixeltype </span> </p> </th> 
   <th colname="col3" class="entry"> <p>回應MIME型別 </p> </th> 
   <th colname="col4" class="entry"> <p>內嵌ICC設定檔 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg， jpg </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png， png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8， png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif， tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg)、pathEmbed=、qlt </span> </p> <p>( <span class="codeph"> qlt= </span> 被忽略，除非 <span class="varname"> tiffCompression </span> 設為'jpeg'。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf， swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p>(Flash Player會忽略內嵌的ICC設定檔。) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>， <span class="codeph"> 屬性：：TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg)，qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> 被忽略，除非 <span class="varname"> tiffCompression </span> 設為'jpeg'。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif， gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>（資料在轉換為灰色或rgb後，會轉換為調色盤。） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

指定傳送至使用者端的回覆影像資料的編碼格式，以及HTTP回覆標頭的對應回應MIME型別。

`png-alpha` 傳回未關聯的Alpha （即Alpha不會預先乘以畫素值），而 `tif-alpha`、和 `swf-alpha` 傳回相關的alpha （即alpha值會與alpha值預先相乘）。 Alpha色版對應至暈映背景遮色片的反面 `req=img`，以及至群組或物件遮色片（如果有） `req=object`. 若要在使用巢狀IR請求時套用Alpha，請新增 `fmt=` 內嵌IR請求和主要請求的適當alpha檔案格式。 如果指定CMYK或灰階ICC設定檔，則不會傳回Alpha資料 `icc=`.

## 屬性 {#section-eb12a82c69d84622bcea153dd84d95b3}

可能發生在請求中的任何位置。

## 默认 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 預設為 `attribute::Format`和 *`tiffCompression`* 預設為 `attribute::TiffEncoding`. *`pixelType`* 預設為 `rgb` 如果 `icc=` 未指定，否則會對應到指定ICC設定檔的畫素型別。

## 另请参阅 {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute：：Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ， [attribute：：JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)， [attribute：：TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e)， [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)， [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)， [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)， [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)， [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
