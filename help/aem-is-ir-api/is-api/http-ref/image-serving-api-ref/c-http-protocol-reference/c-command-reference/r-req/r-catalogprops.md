---
description: 影像目錄屬性。 傳回要求路徑中指定的影像目錄的一般屬性。
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 11%

---

# catalogprops{#catalogprops}

影像目錄屬性。 傳回要求路徑中指定的影像目錄的一般屬性。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

擷取預設目錄屬性( [!DNL default.ini])，省略目錄ID。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.

系統會傳回下列屬性值：

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> 属性</b> </td> 
   <td> <b> 类型</b> </td> 
   <td> <b> 對應的目錄屬性</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：defaultExt</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph"> attribute：：DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph"> attribute：：DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：LastModified</span>、或（如果不存在）的上次修改時間 <span class="varname"> 目錄</span><span class="filepath"> .ini</span> 檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int，bool </p> </td> 
   <td> <p> <span class="codeph"> attribute：：JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph"> attribute：：MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> attribute：：PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：浮水印</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
