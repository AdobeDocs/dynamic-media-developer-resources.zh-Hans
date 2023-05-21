---
description: 「影像伺服」支援以規則運算式相符和替代規則為基礎的簡單請求前置處理機制。
solution: Experience Manager
title: 規則集參考
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# 規則集參考{#rule-set-reference}

「影像伺服」支援以規則運算式相符和替代規則為基礎的簡單請求前置處理機制。

預先處理規則的集合(*規則集*)可附加至影像目錄或預設目錄。 只有在要求未識別特定的主要影像目錄時，才套用預設目錄中的規則。

請求預先處理規則可在請求由處理之前修改請求的路徑和查詢部分 [!DNL Platform Server]的剖析器，包括操控路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫某些安全性功能，這些功能通常僅由目錄屬性控制，例如請求模糊化、標籤水印，以及將服務限制在特定的使用者端IP位址。

規則集會儲存為XML檔案檔案。 規則集檔案的相對或絕對路徑必須在 `attribute::RuleSetFile`.

## 一般結構 {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

此 `<?xml>` 和 `<ruleset>` 即使未定義實際規則，有效規則集XML檔案中的元素永遠是必要的。

一 `<ruleset>` 包含任意數量的元素 `<rule>` 允許元素。

預先處理規則檔案的內容區分大小寫。

## 規則集驗證 {#section-d8d101a0b4d74580835e37d128d05567}

副本 [!DNL RuleSet.xsd] 在目錄資料夾中提供，且應在中註冊規則集檔案之前，用來驗證該檔案 [!DNL catalog.ini] 檔案。 請注意，「影像伺服」會使用 [!DNL RuleSet.xsd] 以進行驗證。

## URL預先處理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在任何其他處理作業之前，會先對傳入的HTTP要求進行部分剖析，以決定應該套用哪個影像目錄。 識別目錄後，將套用所選目錄（或預設目錄，如果未識別特定目錄）的規則集。

此 `<rule>` 會依照為符合專案指定的順序搜尋元素，該符合專案的內容為 `<expression>` 元素( *`expression`*)。

若為 `<rule>` 符合，選填 *`substitution`* 會套用，而修改後的請求字串會傳遞至伺服器的請求剖析器，以進行正常處理。

如果在結束日期時沒有成功比對 `<ruleset>` 到達時，請求會傳遞至剖析器，而不會進行修改。

## OnMatch屬性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

預設行為可修改 `OnMatch` 的屬性 `<rule>` 元素。 `OnMatch` 可設為 `break` （預設）， `continue`，或 `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>元素和屬性</b> </th> 
   <th class="entry"> <b>發生相符時的行為</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>在套用此規則的替代之後，規則處理會立即終止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>會套用替代，並會繼續處理下一個規則。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>規則處理會立即終止，且「已拒絕要求」回應狀態會傳回給使用者端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆寫目錄屬性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

此 `rule` element可選擇性地定義屬性，以在成功比對規則時覆寫對應的目錄屬性。 如果有多個相符的規則設定了相同的屬性，則最後一個規則會優先。 另請參閱 [規則](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 可用規則控制的屬性清單的元素。

## 規則運算式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

簡單字串比對適用於非常基本的應用程式，但在大多數情況下都需要規則運算式。 雖然規則運算式是符合業界標準的，但具體的實施會因執行個體而異。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 說明「影像伺服」使用的特定規則運算式實施。

## 擷取的子字串 {#section-066e659406d5403599cd26ae35e80d68}

為了便於修改複雜的URL，您可以在運算式中透過以括弧(...)括住子字串來擷取子字串。 擷取的子字串會根據前導括弧的位置，從1開始依序編號。 擷取的子字串可以使用插入替代中 ` $ *`n`*`，其中 *`n`* 是擷取的子字串的序號。

## 管理規則集檔案 {#section-0598a608e4044bb4805fe93ceebe10a9}

一個規則集檔案可附加至每個具有目錄屬性的影像目錄 `attribute::RuleSetFile`. 雖然您可以隨時編輯規則集檔案，但影像伺服器只有在重新載入關聯的影像目錄時，才會辨識變更。 當平台伺服器啟動或重新啟動時，以及每當主要目錄檔案(具有 [!DNL .ini] 檔案字尾)修改或「接觸」以變更檔案日期。

## 示例 {#section-aa769437d967459299b83a4bf34fe924}

**範例A.** 如果影像名稱具有字尾「 」，請定義增加影像品質設定的規則 [!DNL _hg]「：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

規則運算式會指定「」的相符專案（不區分大小寫） [!DNL _hg]」於URL字串結尾。 字尾會取代為指定的查詢字串，而這會變更影像品質設定。 請注意 `?` 替代字串中的字元會逸出，因為這是規則運算式中的特殊字元。

>[!NOTE]
>
>&amp;字元所需的編碼。 或者，替代字串可以包含在CDATA區塊中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**範例B。** 特定網頁應用程式不允許查詢字串。 定義翻譯結尾路徑元素的規則 `small`， `medium`，或 `large` 至範本，使用路徑的其餘部分作為影像名稱。 例如， `myCat/myImage/small` 將轉換為 `myCat/smallTemplate?src=myCat/myImage`.

我們可以使用子字串來重新建構請求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另请参阅 {#section-9b748e7c5cff4759a70f96657bd43352}

[套件java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
