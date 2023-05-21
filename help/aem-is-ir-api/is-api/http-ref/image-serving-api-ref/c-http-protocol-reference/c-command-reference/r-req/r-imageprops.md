---
description: 來源影像屬性。 傳回URL路徑中指定的影像檔案或目錄專案的選取屬性。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 10%

---

# imageprops{#imageprops}

來源影像屬性。 傳回URL路徑中指定的影像檔案或目錄專案的選取屬性。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

請求字串中的其他命令會被忽略。

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.

傳回下列屬性：

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> 属性</b> </td> 
   <td> <b> 类型</b> </td> 
   <td> <b> 说明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph"> catalog：：錨點</span> 或預設錨點 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 双 </p> </td> 
   <td> <p> <span class="codeph"> catalog：：到期</span> 或預設存留時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>以畫素為單位的完整解析度影像高度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此影像相關聯的設定檔名稱/說明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 （如果關聯的設定檔內嵌在影像中） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1如果影像包含Photoshop路徑資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. embeddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 (如果影像包含XMP資料) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 0代表無遮色片，1代表預乘alpha，2代表非預乘alpha，而3代表個別的遮色片影像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> catalog：：Modifier</span> 如果不是目錄專案，則為空白 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. photoshopPathNames</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此影像相關聯的所有Photoshop路徑名稱清單（以逗號分隔） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像型別，可以是'CMYK'、'RGB'或'BW' （適用於灰階影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> attribute：：PostModifier</span> 如果不是目錄專案，則為空白 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> 預設列印解析度（畫素/英吋） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> catalog：：Resolution</span> 或預設物件解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>修改日期/時間(從 <span class="codeph"> catalog：：TimeStamp</span> 或影像檔案) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：ThumbRes</span> 或預設縮圖解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：ThumbType</span> 或預設縮圖型別 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 以畫素為單位的完整解析度影像寬度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 目錄ID的 <span class="varname"> 物件</span> 路徑中指定的已解析(請參閱 <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> 物件ID轉譯</a>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>
