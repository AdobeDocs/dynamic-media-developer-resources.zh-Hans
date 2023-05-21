---
description: 「影像伺服」提供一種機制，可將外部物件ID轉譯為地區設定的特定物件（目錄） ID。 主要應用程式是用來提供地區設定特定內容以及在多個地區設定之間共用的內容，使用者端應用程式不需要知道地區設定特定物件ID。
solution: Experience Manager
title: 物件ID翻譯
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 物件ID翻譯{#object-id-translation}

「影像伺服」提供一種機制，可將外部物件ID轉譯為地區設定的特定物件（目錄） ID。 主要應用程式是用來提供地區設定特定內容以及在多個地區設定之間共用的內容，使用者端應用程式不需要知道地區設定特定物件ID。

只要使用全域物件ID即可編寫應用程式，而「影像伺服」會自動取代地區設定的特定影像和其他可用內容。

此 *`locale`* 的影像伺服請求中指定的 `locale=` 命令。

>[!NOTE]
>
>物件ID轉譯僅適用於以目錄為基礎的「影像伺服」使用。 無法轉譯檔案名稱。

## 范围 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

對影像、SVG和靜態內容目錄中的專案的所有參照都被視為翻譯字型，而ICC設定檔參照則不翻譯。 除了 *`object`* 在路徑中 [!DNL /is/image] 和 [!DNL /is/static requests]，這些命令和目錄屬性可能會受到ID轉譯的限制： `src=`， `mask=`， `template=`， `defaultImage=`， `attribute::DefaultImage`、和 `attribute::Watermark`.

## ID轉譯對應 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 定義伺服器用來決定本地化內容ID的規則，以輸入一般物件ID和 `locale=` 值。

`attribute::LocaleMap` 由輸入清單組成 *地區設定* (符合以下專案指定的值： `locale=`)，每個區域設定尾碼都不含或超過輸出( `*`locsuffixes`*`)。

例如， `attribute::LocaleMap` 可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

請求 `/is/image/myCat/myImg?locale=de_de` 會傳回與目錄專案關聯的影像 `myCat/myImg_D` （假設此類目錄專案存在）。

請參閱 `attribute::LocaleMap` 以取得詳細資訊。

## 翻譯程式 {#section-1f64db17e9f644d88e09853670e14a16}

根據上述範例，伺服器會先尋找 *`locale`* &quot; `de_de`&quot; （在ID翻譯對應中）。 然後它會反複執行 *`locSuffixes`* 與此專案相關聯 — 在此案例中為&quot; `_D`&quot;和&quot;&quot; （空白尾碼）。 對於每個反複專案，字尾都會附加至影像ID，而產生的ID會根據目錄中的存在性進行測試。 如果找到，則會使用該目錄專案，否則會測試下一個目錄專案。 在此範例中，會勾選下列專案： `myCat/myImg_D`、和 `myCat/myImg`. 如果找不到相符專案，伺服器會傳回錯誤或預設影像（如果已設定）。

## 未知的語言環境 {#section-b2f3c83f2dc845d69b5908107b775537}

在上述範例中， `attribute::LocaleMap` 包含空白 *`locale`* 定義預設翻譯規則，用於未知 `locale=` 值（即未在翻譯對應中明確列出的值）。 如果此翻譯對應已套用至要求 `/is/image/myCat/myImg?locale=ja`，則它會 `myCat/myImg_E`，若有的話，否則 `myCat/myImg`.

如果翻譯對應未指定預設翻譯規則，則會為所有不明請求傳回錯誤 `locale=` 值。

## 示例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多層級查詢**

通常希望將地區設定（例如，歐洲、中東、北美）分組以符合地區標準。 這可以透過多層級查詢來達成。

在此範例中，我們要支援收藏集供西方和中東使用。 这两个集合都基于通用图像集合，而且都添加或修改某些图像。然後針對特定地區設定進一步調整這兩個集合( `m1`， `m2` 兩個中東變體的，以及 `w1`， `w2`、和 `w3` （3種西方語言環境），但影像會共用給 `w1` 和 `w3`. 未知区域设置仅映射到通用集合，而且无法访问区域设置特定的图像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表說明考慮的目錄專案，以及考慮一般輸入ID的目錄專案順序 `myImg`：

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>要搜尋的目錄ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> 我的影像 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜尋特定ID**

某些影像命名慣例在內部可能不支援一般影像ID。 要求中的通用ID必須一律對應至目錄中的特定ID；通常可能不知道確切的特定ID。

在此範例中，所有語言的影像可能都有 `_1`， `_2`，或 `_3` 字尾。 法語地區設定的特定影像可能有 `_22` 或 `_23` 字尾，以及德文地區設定的特定影像 `_470` 或 `_480` 字尾。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表說明考慮的目錄專案，以及考慮一般輸入ID的目錄專案順序 `myImg`：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>要搜尋的輸出ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>， <span class="codeph"> de_at </span>， <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另请参阅 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ， [attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
