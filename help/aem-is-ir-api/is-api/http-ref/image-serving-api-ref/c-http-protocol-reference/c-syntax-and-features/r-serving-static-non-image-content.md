---
description: 提供靜態（非影像）內容
solution: Experience Manager
title: 提供靜態（非影像）內容
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 提供靜態（非影像）內容{#serving-static-non-image-content}

「影像伺服」提供一種機制，可管理目錄中的非影像內容，並透過個別的伺服器提供 `context /is/content`. 此機制允許分別為每個專案設定TTL。

## 基本語法 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 請求 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> 伺服器 </span>/is/content[/ <span class="varname"> 目錄 </span>/ <span class="varname"> 個專案 </span>][？ <span class="varname"> 修飾元 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[： <span class="varname"> 連線埠 </span>] </span> </p> </td> 
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

## 命令概述 {#section-61657a0141914053ab12038ad7e91500}

「影像伺服」支援/is/content的下列命令：

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> 类型 </a> </td> 
  <td class="stentry"> <p>內容型別篩選器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> 需要 </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>， <span class="codeph"> req=props </span>、和 <span class="codeph"> req=exists </span> 僅限。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> 快取 </a> </td> 
  <td class="stentry"> <p>允許停用使用者端快取。 </p> </td> 
 </tr> 
</table>

## 靜態內容目錄 {#section-b2b8f4860fe84e528493ed704c7c5141}

靜態內容目錄與影像目錄類似，但支援的資料欄位較少：

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 屬性/資料</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：Id </span> </p> </td> 
   <td> <p> 此靜態內容專案的目錄記錄識別碼 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：Path </span> </p> </td> 
   <td> <p> 此內容專案的檔案路徑 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：到期 </span> </p> </td> 
   <td> <p> 如果未指定或為空，則會使用這個內容專案；屬性：：Expiration的TTL </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：TimeStamp </span> </p> </td> 
   <td> <p> 檔案修改時間戳記；使用attribute：：CacheValidationPolicy啟用目錄型驗證時需要 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td> <p> 與此靜態內容專案關聯的可選中繼資料；適用於具有req=userdata的使用者端 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：UserType </span> </p> </td> 
   <td> <p> 選擇性資料型別；可用來透過type=命令篩選靜態內容的請求 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-896c37cf68bc446eb0766fb378898262}

此機制可協助確保使用者端僅接收適合其需求的內容。 假設靜態內容已使用適當標籤 `catalog::UserType`值，使用者端可新增 `type=` 命令到要求。 「影像伺服」會比較 `type=` 命令至的值 `catalog::UserType` 若不相符，則傳回錯誤而非可能不適當的內容。

## 另请参阅 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ， [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [影像目錄參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
