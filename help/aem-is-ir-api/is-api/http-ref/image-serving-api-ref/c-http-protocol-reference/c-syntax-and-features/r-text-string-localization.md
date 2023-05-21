---
description: 文字字串本地化可讓影像目錄包含相同字串值的多個地區設定特定表示法。
solution: Experience Manager
title: 文字字串本地化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 3%

---

# 文字字串本地化{#text-string-localization}

文字字串本地化可讓影像目錄包含相同字串值的多個地區設定特定表示法。

伺服器會將符合指定之地區設定的表示傳回給使用者端 `locale=`，因此可避免使用者端本地化，並允許應用程式只要傳送適當的 `locale=` IS文字要求的值。

## 范围 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文字字串本地化會套用至包含本地化權杖的所有字串元素 ` ^loc= *`locId`*^` 在下列目錄欄位中：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目錄欄位</b> </th> 
   <th class="entry"> <b>欄位中的字串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Imageset </span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（以分隔符號「，」「；」「：」和/或欄位開頭/結尾的任何組合分隔）。 </p> <p> A <span class="codeph"> 0xrrggbb </span> 可本地化欄位開頭的顏色值會排除在本地化之外，並在未修改的情況下傳遞。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Map </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，除了 <span class="codeph"> 色彩= </span> 和 <span class="codeph"> shape= </span> 屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：目標 </span> </p> </td> 
   <td> <p>任何值 <span class="codeph"> 目標。*.label </span> 和 <span class="codeph"> 目標。*.userdata </span> 屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字串語法 {#section-d12320edf300409f8e17565b143acafc}

已啟用本地化 *`string`* 影像目錄中的元素包含一或多個當地語系化的字串，每個字串前面都有一個當地語系化代號。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> 預設字串 </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locstr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>的內部地區設定ID <span class="varname"> localizedString </span> 關注此 <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化的字串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 預設字串 </span> </span> </p> </td> 
  <td class="stentry"> <p>用於未知地區設定的字串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必須是ASCII且不得包含「^」。

不論是否使用HTTP編碼，&#39;^&#39;都可能出現在子字串中的任何位置。 伺服器符合整個 *`localizationToken`* `^loc=locId^` 分隔子字串的模式。

*`stringElements`* 其中至少不包含一個 *`localizationToken`* 不建議本地化。

## 翻譯地圖 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定義伺服器用來判斷哪一個的規則 *`localizedStrings`* 以返回使用者端。 它由輸入清單組成 *`locales`* (符合以下專案指定的值： `locale=`)，每個區段都沒有任何或多個內部地區設定ID ( *`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空白 *`locId`* 值表示 *`defaultString`* 應該會傳回（如果有的話）。

請參閱 `attribute::LocaleStrMap` 以取得詳細資訊。

## 翻譯程式 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

根據以上範例翻譯對應和請求 `/is/image/myCat/myItem?req=&locale=nl`，伺服器會先尋找&quot; `nl`&quot; （在地區地圖中）。 相符的專案 `nl,N` 表示針對每個 *`stringElement`*，則 *`localizedString`* 標示為 `^loc=N^` 應該會傳回。 若此 *`localizationToken`* 不存在於 *`stringElement`*，則會傳回空值。

假設 `catalog::UserData` 的 `myCat/myItem` 包含下列內容（為了清楚起見，插入了分行符號）：

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

伺服器會傳回下列內容，以回應範例要求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知的語言環境 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上述範例中， `attribute::LocaleStrMap` 有一個專案包含空白 *`locale`* 值。 伺服器使用此專案處理所有 `locale=` 翻譯對映中未明確指定的值。

範例翻譯對應會指定在此情況下， *`defaultString`* 應該會傳回（如果有的話）。 因此，若將此翻譯對應套用至請求，將會傳回以下內容 `/is/image/myCat/myItem?req=&locale=ja`：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 示例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**語言系列**

多個 *`locId`* 值可與每個 *`locale`* 在翻譯地圖中。 這可支援特定國家或地區的特定變數（例如美式英文與英式英文） *`stringElements`* 處理大多數內容時所使用的共同基本語言環境（例如國際英文）。

舉例來說，我們想要新增美國專屬英文的支援( `*`locId`* EUS`)和英國特有英文( `*`locId`* EUK`)，以支援偶爾使用的替代拼字。 如果EUK或EUS不存在，我們會回溯為E。同樣地，奧地利特有德文變體( `DAT`)可於需要時提供使用，同時傳回一般德文 *`localizedStrings`* (標籤有 `D`)大部分時間。

`attribute::LocaleStrMap` 將如下所示：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表說明部分代表的輸出 *`stringElement`* 和 *`locale`* 組合：

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>輸出字串 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Audiential </span> </p> </td> 
   <td> <p> en， en_us </p> <p> en_uk </p> <p> de， de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>UK — 英文 </p> <p>德文 </p> <p>奧地利文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 請注意，在此範例中， <span class="varname"> locId </span> DDE不存在於 <span class="codeph"> attribute：：LocaleStrMap </span>，因此就是與此關聯的子字串 <span class="varname"> locId </span> 不會傳回。 </p> </td> 
   <td> <p> en， en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>美式英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
