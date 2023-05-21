---
title: 提供靜態（非影像）內容
description: 您可以使用「影像伺服」來管理目錄中的非影像內容，並透過個別的/is/content內容內容來提供。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# 提供靜態（非影像）內容{#serving-static-non-image-contents}

您可以使用「影像伺服」來管理目錄中的非影像內容，並透過個別的/is/content內容內容來提供。

此功能允許分別為每個專案設定TTL。

「影像伺服」支援以下命令： [!DNL /is/content]：

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 类型 </a> </p> </td> 
  <td class="stentry"> <p>內容型別篩選器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> 需要 </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>， <span class="codeph"> req=props </span>、和 <span class="codeph"> req=exists </span> 僅限。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 快取 </a> </p> </td> 
  <td class="stentry"> <p>允許停用使用者端快取。 </p> </td> 
 </tr> 
</table>

## 基本語法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 請求 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> 伺服器 </span>/is/content[/catalog/ <span class="varname"> 個專案 </span>][？ <span class="varname"> 修飾元 </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ ： <span class="varname"> 連線埠 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目錄 </span> </span> </p> </td> 
  <td class="stentry"> <p>目錄識別碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 個專案 </span> </span> </p> </td> 
  <td class="stentry"> <p>靜態內容專案ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾元 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span>*[&amp; <span class="varname"> 命令 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> 值 </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>支援的命令名稱之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 靜態內容目錄 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

靜態內容目錄與影像目錄類似，但支援的資料欄位較少：

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性/資料 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：Id </span> </p> </td> 
   <td colname="col2"> <p>此靜態內容專案的目錄記錄識別碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：Path </span> </p> </td> 
   <td colname="col2"> <p>此內容專案的檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：到期 </span> </p> </td> 
   <td colname="col2"> <p>此內容專案的TTL； <span class="codeph"> attribute：：Expiration </span> 如果未指定或為空，則會使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>檔案修改時間戳記；使用啟用目錄型驗證時需要 <span class="codeph"> attribute：：CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td colname="col2"> <p>與此靜態內容專案關聯的可選中繼資料；適用於具有下列專案的使用者端： <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：UserType </span> </p> </td> 
   <td colname="col2"> <p>選用資料型別；可用於篩選靜態內容的請求，具有 <span class="codeph"> type=命令 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-4c41bf41ff994910840c1352683d1f37}

此機制可協助確保使用者端僅接收適合其需求的內容。 假設靜態內容已使用適當標籤 `catalog::UserType` 值，使用者端可新增 `type=` 命令到要求。 「影像伺服」會將提供的值與 `type=` 命令至的值 `catalog::UserType` 而且，如果兩者不相符，則會傳回錯誤，而非可能不適當的內容。

## 視訊註解檔案 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

您可以封裝視訊註解檔案(WebVTT)、CSS或JSONP格式的任何文字檔。 JSON回應如下所述。

* 對於WebVTT檔案，回應的mime型別是text/javascript。 系統不會傳回JSON，而是會傳回JavaScript，以便呼叫具有JSON的方法。 ID和處理常式都是選用的。
* 對於CSS檔案，回應的mime型別是text/javascript。 ID和處理常式都是選用的。
* 依預設，會套用UTF-8編碼，以確保正確解碼。 預設大小限製為2 MB。

您也可以將追蹤用於其他型別的計時中繼資料。 每個曲目元素的來源資料都是由計時提示清單組成的文字檔。 提示可包括JSON或CSV等格式的資料。

另請參閱 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 以取得有關JSONP格式的詳細資訊。

另請參閱 [www.json.org](https://www.json.org/json-en.html) 以取得有關JSON格式的詳細資訊。

## 另请参阅 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ， [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [影像目錄參考](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
