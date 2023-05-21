---
description: 來源物件規範。 可以將影像、SVG和ICC設定檔物件指定為影像目錄專案或相對檔案路徑
solution: Experience Manager
title: 对象
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# 对象{#object}

來源物件規範。 可以將影像、SVG和ICC設定檔物件指定為影像目錄專案或相對檔案路徑

`*`物件`*[/]{[ *`rootId`*/] *`物件ID`*}| *`路徑`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>影像目錄的名稱( <span class="codeph"> attribute：：RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主要或預設影像目錄中的影像、SVG、範本或ICC設定檔記錄的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路徑 </span> </span> </p> </td> 
  <td class="stentry"> <p>相對影像、遮色片或ICC設定檔檔案路徑與名稱 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物件 </span> </span> </p> </td> 
  <td class="stentry"> <p>可能發生在主要URL路徑中，或在 <span class="codeph"> src= </span>， <span class="codeph"> 遮色片= </span>，或 <span class="codeph"> icc= </span> 命令 </p> </td> 
 </tr> 
</table>

*`rootId`* 會識別影像目錄。 (請參閱 [影像目錄](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 以取得詳細資訊。) 若 *`rootId`* 在URL路徑中指定，則該目錄會變成 *主要目錄* 以取得此要求。 否則，預設目錄會作為主目錄使用。 同一個請求中可以使用多個不同的影像目錄。

伺服器最初假設 *`rootId`* 中省略 `src=`， `mask=`、和 `icc=` 和會嘗試在主目錄中尋找目錄專案。 實際上，伺服器會嘗試使用整個 *`object`* 字串為 *`objId.`*

如果找到目錄專案，則會使用它；否則，伺服器會接著嘗試比對 *`rootId`* 影像目錄的。 如果識別了目錄，則會搜尋該目錄 *`objId`*. 如果找到和專案，則會使用它。

否則， *`object`* 會假設為明確的檔案路徑。 在此情況下，如果 `attribute::FullMatch` 在主目錄中設定時，則會忽略此物件的目錄，並改用預設目錄。 若 `attribute::FullMatch` 未設定，則會使用主目錄進行進一步處理。

兩者 *`rootId`* 和 *`objId`* 區分大小寫。 *`path`* 僅在UNIX上區分大小寫。

如果行距 `/` 指定，則會搜尋預設目錄，而非主目錄。 當明確路徑需要 `default::RootPath` 而不是主目錄的 `attribute::RootPath`，但也可用來存取預設目錄中的專案，否則這些專案會被主目錄中的專案覆寫。

請參閱 *管理內容* 在 *伺服器設定指南* 以取得如何進行 *`path`* 會轉換為實體檔案路徑。

>[!NOTE]
>
>逗號&#39;，&#39;字元不允許出現在 *`object.`*

## 支援的影像檔案格式 {#section-12c85aead78e4f759856ca9ff10637d7}

如需支援的檔案格式完整清單，請參閱IC （影像轉換程式）公用程式的說明。

需要多個不同解析度的影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIF)多解析度格式時表現最佳。 IC公用程式可用來從任何支援的影像格式建立PTIF影像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**存取兩個不同影像目錄中的影像和ICC設定檔**

擷取影像&#39; [!DNL myImage]在影像目錄中的「 」識別為「 [!DNL myCatalog]&#39;並附加ICC設定檔&#39; [!DNL sRGB]&#39;位於名為&#39;的影像目錄中 [!DNL myProfiles]&#39;：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用單一影像目錄進行分層

**建立包含三個圖層的簡單複合影像，全部擷取自&#39; [!DNL myCatalog]&#39;：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接存取影像檔案，同時仍使用目錄來提供屬性**

存取 [!DNL my/image/path/myImage.tif]，使用中設定的預設jpg屬性 `myImageCatalog`：

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[積體電路公用程式](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)， [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [attribute：：FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
