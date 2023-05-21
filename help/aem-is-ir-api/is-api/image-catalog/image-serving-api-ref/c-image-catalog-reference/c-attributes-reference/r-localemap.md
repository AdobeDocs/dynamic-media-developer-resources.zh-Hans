---
description: ID翻譯對應。 指定用來將一般影像ID轉譯為地區設定特定ID的規則。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID翻譯對應。 指定用來將一般影像ID轉譯為地區設定特定ID的規則。

`*`個專案`*&#42;['|' *`個專案`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 项目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>，<span class="varname"> locSuffix</span>*['，'<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>地區設定ID （不區分大小寫）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>地區設定字尾。 </p></td> 
 </tr> 
</table>

`LocaleMap` 是指 `locId` 可對應至任意數量的 `locSuffix`.

空白 *`locSuffix`* 允許使用值。 *`locSuffix`* 值必須依其搜尋順序排序。 傳回第一個相符項。

「影像伺服」搜尋 *`locId`* 不區分大小寫的值會與 `locale=` 請求中指定的值。 如果找到相符專案，則第一個相關聯的 *`locSuffix`* 值會附加至原始目錄id。 如果此目錄專案存在，則會使用它，否則會使用下一個 *`locSuffix`* 已嘗試值。 如果沒有 *`locSuffix`* 值與目錄專案相符，影像伺服會傳回錯誤或預設影像。

空白 *`locId`* 值符合空白和未知 `locale=` 字串。 這允許為未知地區設定定義預設規則。

ID轉譯在啟用時，會套用至參考影像目錄和靜態內容目錄專案的所有ID。

## 屬性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一或多個專案，以分隔 |，其中每個專案都包含兩個或多個以逗號分隔的字串值。 *`locId`* 和 `locale=` 會比較。 不區分大小寫。

## 另请参阅 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支援， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [attribute：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
