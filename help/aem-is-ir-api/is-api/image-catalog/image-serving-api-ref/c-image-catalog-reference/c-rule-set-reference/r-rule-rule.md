---
title: 规则
description: 要求規則元素。 一或多個規則是選用的， <ruleset> 元素。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 6%

---

# 规则{#rule}

要求規則元素。 一或多個規則是選用的， `<ruleset>` 元素。

## 属性 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 可选. 預設值為「break」。

`Replace = "first" | "all"`: 可选. 預設值為「first」。

`RequestType` = *&quot;`types`&quot;*：選擇性。 指定套用規則的輸入內容。 *`types`* 是以逗號分隔的清單，可能包含下表所列的一或多個代號。 若 `RequestType` 未指定，則規則會套用至在所有支援的內容上收到的請求。

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>令牌</b> </p> </th> 
   <th class="entry"> <p><b>內容</b> </p> </th> 
   <th class="entry"> <p><b>说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 是</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>套用至影像伺服請求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>已套用至影像演算要求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 静态</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>套用至靜態內容請求 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: 可选. 用於識別 `<rule>` 偵錯記錄檔和錯誤訊息中的元素。

`  *`屬性`* ="value"`：選擇性。 `<rule>` 元素可以任意組合來定義下列任何屬性。 如果已指定，且規則已成功比對，則將覆寫此請求的對應目錄屬性。 默认值为 `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> 屬性 </span> </b> </th> 
   <th class="entry"> <p>對應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 預設影像模式</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> 屬性：：DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute：：ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 过期时间</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> attribute：：Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> attribute：：MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute：：RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 要求模糊化</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> 屬性：：RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute：：RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 儲存路徑</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> attribute：：SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 水印</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribute：：WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

如需詳細資訊，請參閱對應影像目錄屬性的說明。

到期屬性只會覆寫預設屬性值。 如果特定的 `catalog::Expiration` 值會套用至要求。

## 数据 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
</table>

## 说明 {#section-0c5fbc363070419d8c9800b0c02dc9f9}

若兩者皆有 `<expression>` 和 `<substitution>` 中指定的子字串，且不會使用擷取的子字串，則第一個相符的子字串會取代為 `<substitution>`.

若 `<expression>` 未指定，任何路徑皆符合和 `<substitution>` 會附加至路徑的結尾。

若 `<substitution>` 未指定，不會發生路徑或查詢轉換，但會覆寫任何指定的目錄屬性。 若 `<substitution>` 空白，則會移除相符的子字串。

此 `<addressfilter>` 只會在符合發生時套用，並在套用查詢規則之前套用。
