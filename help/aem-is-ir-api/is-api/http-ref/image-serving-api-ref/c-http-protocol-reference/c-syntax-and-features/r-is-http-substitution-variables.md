---
description: 替代變數可用來將請求URL中的值傳輸至合成影像目錄中儲存的範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替代變數可用來將請求URL中的值傳輸至合成影像目錄中儲存的範本。 變數也可用來將相同的值傳達給複雜請求中的不同位置。

` $ *`var`*= *`值`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

變數定義和參考可能會出現在請求的查詢部分，位於 `catalog::Modifier`、和 `catalog::PostModifier`.

變數的定義如上所述，與其他IS命令類似；前導的「$」會將該命令識別為變數定義。 必須先定義變數，才能加以參照。

變數名稱 *`var`* 不區分大小寫，而且可能包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任何組合。

>[!NOTE]
>
>*`value`* 必須為單通道URL編碼，才能安全HTTP傳輸。 在以下情況中需要雙重編碼 *`value`* 會透過HTTP重新傳輸。 情況如下： *`value`* 會取代為巢狀外部請求或SVG的href屬性 `<image>` 元素。

變數參考是由開頭與結尾為「$」($)的變數名稱所組成&#x200B;*var*$)。 參考可能出現在任何IS命令的值部分中的任何位置（即命令名稱后面的&#39;=&#39;和後續的&#39;&amp;&#39;或請求結尾之間）。 自訂變數無法套用至 `layer=` 和 `effect=` 命令。 相同命令值中允許多個變數。 伺服器會取代以下專案的每個專案： ` $ *`var`*$` 替換為 *`value`*.

變數參考不可巢狀。 任何出現次數 ` $ *`var`*$` 範圍 *`value`* 不會被取代。

例如，請求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析為：

`text=my$var2$tree`

>[!NOTE]
>
>「$」不是保留字元；它可能會出現在請求中的其他位置。 例如， `src=my$image$file.tif` 是有效的命令(假設目錄專案或影像檔案名為 `my$image$file.tif` 存在)，而 `wid=$number$` 不是，因為 `wid` 需要數值引數。

## 巢狀請求中的變數處理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 參考可能會出現在巢狀影像提供或影像轉譯請求的大括弧內的任何位置，包括在「？」的左側 將路徑與查詢分開。 伺服器會以（來自url或的）值取代這些參考 `catalog::Modifier` 進一步剖析及處理巢狀要求之前，請先檢查巢狀要求是否存在。

此外，所有 ` $ *`var`*=` url中的定義或 `catalog::Modifier` 轉送至所有巢狀影像伺服和影像演算請求。 這樣可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀內嵌層級為何，只有單次HTTP編碼必須套用至變數值，而要在巢狀影像演算或影像伺服請求或其關聯中的任何位置取代 `catalog::Modifier` 字串。

## 內嵌外部請求中的變數處理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 內嵌外部請求大括弧內任何位置的參考，會以相符的變數定義值取代。 這允許將內嵌的外部請求放置在影像目錄的範本中。

要取代成外部請求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部URL之前不會套用重新編碼。

## SVG檔案中的變數處理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 引用可能會出現在屬性值和SVG檔案中 `<text>` 字串。 「影像伺服」會以相符專案取代這些專案 ` $ *`var`*=` 在指定SVG檔案的請求巢狀層級中已知的定義。

>[!NOTE]
>
>要取代的任何變數值 `href` 屬性值必須經過兩次URL編碼；所有其他值都必須經過單獨編碼。

## 預先定義的路徑變數 {#section-930d0dd12e8f49499becc9fe8df24092}

此 *`object`* 請求路徑中指定的會指派給預先定義的變數 `*`$object`*`. &#39; ` $ *`物件`*$`&#39;可放置在請求中的任意位置、請求所參考的範本中，或允許此類物件的巢狀/內嵌請求中，包括 `src=` 和 `mask=`，以及巢狀/內嵌請求的路徑。

例如，下列請求會重複使用路徑中指定的影像，做為巢狀請求中圖層的來源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

這相當於

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

的定義 `*`$object`*` 可透過明確指定覆寫 ` $ *`物件`*=` ，並提供所需的值。

預先定義的路徑變數通常會與 `template=`.

## 默认 {#section-b02483d15529444586a2e9504805b155}

无. 只有已定義的變數才會由伺服器取代（預先定義的路徑變數$object除外，此變數一律會被取代）。 任何出現次數 ` $ *`var`*$` 若為，則保持常值 `*`var`*`無法與現有變數定義比對。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

請參閱中的「範例A」 [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
