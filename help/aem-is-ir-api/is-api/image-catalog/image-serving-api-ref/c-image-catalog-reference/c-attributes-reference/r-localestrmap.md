---
description: 字串翻譯對應。 參考可對應至任何數目internalLocId的locId。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# LocaleStrMap{#localestrmap}

字串翻譯對應。 參考可對應至任何數目internalLocId的locId。

`*`個專案`*&#42;['|' *`個專案`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 项目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> 地區設定 </span>， <span class="varname"> locId </span>*['，' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>地區設定（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>內部地區設定ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指 `locId` 可對應至任意數量的 `internalLocId`.

空白 *`locale`* 值符合空白和未知 `locale=` 字串。 這允許為未知地區設定定義預設規則。

空白 *`locId`* 允許值並選取 *`defaultString`* (此 *`defaultString`* 沒有地區設定識別碼)。 *`locId`* 系統會依指定的順序搜尋值。 傳回第一個相符項。

字串轉譯在啟用時，會套用至下列影像目錄欄位中的文字字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> <b>欄位中的字串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：Imageset </span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（以分隔符號「，」「；」「：」和/或欄位開頭/結尾的任何組合分隔）。 </p> <p>A <span class="codeph"> 0xrrggbb </span> 可本地化欄位開頭的顏色值會排除在本地化之外，並在未修改的情況下傳遞。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：Map </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，除了 <span class="codeph"> 色彩= </span> 和 <span class="codeph"> shape= </span> 屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：目標 </span> </p> </td> 
   <td> <p>任何值 <span class="filepath"> 目標。*.label </span> 和 <span class="filepath"> 目標。*.userdata </span> 屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8505a8525f6948ada3979f68c4081044}

一或多個專案，以分隔 |，其中每個專案都包含兩個或多個以逗號分隔的字串值。

## 另请参阅 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支援， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)， [catalog：：Imageset](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)， [catalog：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)， [catalog：：目標](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)， [catalog：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
