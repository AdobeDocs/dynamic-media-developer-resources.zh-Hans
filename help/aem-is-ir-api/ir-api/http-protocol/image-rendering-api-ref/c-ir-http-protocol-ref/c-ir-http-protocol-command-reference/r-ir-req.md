---
title: 需要
description: 請求類型. 指定要求的資料型別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# 需要{#req}

請求類型. 指定要求的資料型別。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 偵錯 </span> </p> </td> 
  <td class="stentry"> <p>在偵錯模式下執行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 内容 </span> </p> </td> 
  <td class="stentry"> <p>傳回暈映中物件的相關資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>執行命令並傳回演算後的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>傳回指定暈映的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 地图 </span> </p> </td> 
  <td class="stentry"> <p>傳回內嵌在暈映中的影像地圖資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>執行命令並將已遮罩的演算影像傳回至目前的物件選取範圍。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> prop </span> </p> </td> 
  <td class="stentry"> <p>執行命令並傳回回覆影像的屬性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 使用者資料 </span> </p> </td> 
  <td class="stentry"> <p>傳回以下專案的內容： <span class="codeph"> 暈映：：UserData </span>. </p> </td> 
 </tr> 
</table>

除非在詳細描述中另有說明，否則伺服器會傳回MIME型別的文字回應 &lt;text plain=&quot;&quot;>.

`debug`

執行指定的命令並傳回演算後的影像。 如果發生錯誤，會傳回錯誤和偵錯資訊，而非錯誤影像( `attribute::ErrorImagePath`)。

`contents`

傳回暈映中物件階層的XML表示法，包括選取的物件屬性。 請求中的其他命令會被忽略。

`img`

執行指定的命令並傳回演算後的影像。 回覆資料格式和回覆型別由以下專案決定 `fmt=`.

`imageprops`

傳回URL路徑中所指定暈映檔案或目錄專案的選取屬性。 另請參閱 [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 以取得回覆語法和回應MIME型別的說明。 請求中的其他命令會被忽略。 傳回下列屬性：

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>兩次 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Expiration </span> 或預設存留時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>以畫素為單位的完整解析度高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>與此暈映關聯的設定檔名稱/描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1，表示相關聯的設定檔已內嵌於暈映中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1 （如果暈映嵌入路徑資料）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Modifier </span> 或空白（若不是目錄專案）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>列舉 </p> </td> 
   <td colname="col3"> <p>回應影像的畫素型別；可以是'CMYK'、'RGB'或'BW' （適用於灰階影像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>預設列印解析度（以dpi為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>修改日期/時間(從 <span class="codeph"> catalog：：TimeStamp </span> 或暈映檔案)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>以畫素為單位的完整解析度寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>暈映名稱（根暈映物件的名稱字串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 暈映.res </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>中的最大物件解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材質解析度 </a> 單位（通常是畫素/英吋）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>中的平均物件解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材質解析度 </a> 單位(通常為畫素/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材質解析度 </a>h)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 暈映.res.min </span> </p> </td> 
   <td colname="col2"> <p>實數 </p> </td> 
   <td colname="col3"> <p>中的最小物件解析度 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材質解析度 </a> 單位（通常是畫素/英吋）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>暈映檔案版本號碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

傳回暈映中包含的影像地圖資料。 依預設，會傳回所有最外層群組的對應資料。 可使用取得所有最內層群組的對應資料

`req=map&groupLevel=-1`

對應資料不會縮放至 `wid=` 或 `hei=` 或以其他方式修改。 回應MIME型別為 `<text/xml>`.

回應資料包含 `<map>` 包含一組元素的元素 `<area>` 元素，類似於HTML `<AREA>` 標籤之間。

每個 `<area>` 元素包含標準 `type=` 和 `coord=` 屬性和 `name=` 屬性，指定暈映群組名稱或名稱路徑。 多個 `<area>` 如果對應物件群組的遮色片具有不連續區域，則會出現具有相同名稱的元素。

除了預設屬性之外，暈映可以定義其他屬性（如果編寫的話）。 這類自訂屬性定義為物件群組屬性。 自訂屬性的名稱必須以開頭 `map` 將包含在 `<area>` 元素。 例如，如果群組屬性包括 `map.href=http://www.scene7.com`，對應的 `<area>` 元素包含 `href="http://www.scene7.com"`.

包含空白的XML檔案 `<map>` 如果暈映不包含對應資料，則會傳回元素。

`object`

執行指定的命令，並傳回由剩餘物件選取範圍（最後選取的群組或物件）所遮罩的演算後的影像 `sel=` 或 `obj=` 命令)。 通常與支援Alpha的影像格式搭配使用(請參閱 [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c))。 如果使用不支援Alpha的影像格式，遮色片外的區域為黑色。

`props`

執行指定的命令並傳回暈映屬性和群組或物件屬性，而不是演算後的影像。 另請參閱 [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 以取得回覆語法和回應MIME型別的說明。 除非下列情況，否則將套用預設選取範圍 `obj=` 或 `sel=` 也會指定(請參閱 [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a))。

回應中可能包含以下屬性：

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p> 类型 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回覆影像背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>整型 </p> </td> 
   <td> <p> 回覆影像高度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p>如果ICC設定檔內嵌在回覆影像中，則為True (請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 與回覆影像關聯之設定檔的捷徑名稱(請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回覆影像包含Alpha，則為True。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回覆影像包含路徑資料則為True (請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回覆影像型別，可以是'CMYK'、'RGB'或'BW' （適用於灰階影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 實數 </p> </td> 
   <td> <p> 列印解析度(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整數，布林值 </p> </td> 
   <td> <p> JPEG品質和色度標幟(請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回覆影像的MIME型別(請參閱 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 回覆影像寬度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 目前選取範圍的屬性字串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前選取範圍中的物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前選取範圍的縮排值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 選取 <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 目前物件選取範圍的完整名稱路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlaying </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前選取範圍中的重疊物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p>目前選取範圍中的可轉譯物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前選取範圍中的可紋理物件數目。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前顯示/隱藏目前選取專案的狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 目前選取範圍中第一個重疊物件的Z順序值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

傳回以下專案的內容： `vignette::UserData`. 伺服器會取代所有出現的 `'??'` 在 `vignette::UserData` 帶有行終止元( `<cr><lf>`)。 會將回覆格式化為文字資料，並將回應MIME型別設定為 &lt;text plain=&quot;&quot;>.

如果URL路徑中指定的物件未解析為有效的暈映對應專案，或 `vignette::UserData` 空白，則回覆將僅包含行結束符( `CR/LF`)。

會忽略請求字串中的任何其他命令。

## 屬性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

要求命令。 可能發生在請求字串中的任何位置。

## 默认 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包含影像路徑或修飾元，則：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則， `req=img`

## 另请参阅 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ， [attribute：：ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)， [暈映：：UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)， [屬性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
