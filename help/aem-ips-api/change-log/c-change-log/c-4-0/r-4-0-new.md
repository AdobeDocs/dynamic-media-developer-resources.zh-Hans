---
title: 新增與變更
description: 說明IPS API v4.0的新變更和實施變更。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 2%

---

# 新增與變更{#new-additions-and-changes}

說明IPS API v4.0的新變更和實施變更。

使用不同的WSDL和結構描述名稱空間並排實作API版本。

* 舊版API： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

已新增 `PostScriptOptions/alpha` 欄位。

已新增 `VideoRootUrl` 和 `SwfRootUrl` 屬性 `getProperty` 作業。

新增選用專案 `appName` 和 `appVersion` 引數至 `authHeader` 以追蹤呼叫應用程式。 已新增記錄至 `ipsApiService.log`.

新增選用專案 `serviceUrl` 引數至WSDL產生servlet。 此引數適用於除錯代理。 示例: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已實作 `getZipEntries` 作業。

已實作系統欄位條件的搜尋範圍和輸入的比較值。

已新增 `'Asset'` 資產型別字串常數，主要用於允許跨資產中繼資料欄位。

已實作 `trashState` 引數： `searchAssets`.

已實作 `getAssetPublishHistory` 作業。

新增選用專案 `faultHttpStatusCode` SOAP標頭，可在Flex中啟用錯誤處理。 若為Flex，請使用 `<faultHttpStatusCode>200</faultHttpStatusCode>`. 錯誤回應的預設狀態代碼為 `500 (Internal Server Error)`.

新增從垃圾桶還原資產和從垃圾桶還原空白資產的操作。

實作CRUD作業。

已新增啟用的標幟至 `ImageMap` 型別和 `saveImageMap` 作業。

新增對「最佳化剩餘檔案」工作的支援。

已新增 `setAssetsPublishState` 以取得大量發佈狀態更新。

已新增 `ImageServingPublishSettings`， `getImageServingPublishSettings`， `setImageServingPublishSettings`.

已棄用 `saveMetadataField` 支援新增的作業 `createMetadataField` 和 `updateMetadataField` 作業。

已實作 `deleteAssetsParam` 批次刪除作業。

已實作 `moveAssetsParam` 批次移動作業。

已實作 `deleteMetadataField` 作業。

已實作 `get/setImageRenderingPublishSettings`， `get/set/create/updateVignettePublishFormat` 作業。

已實作 `getAssetCounts`.

新增支援至 `setImageSetMembers` 針對，包括 `RenderSet` 中的成員 `ImageSet` 資產。

已新增 `replaceImage` 作業。

已新增 `copyImage` 作業。

已新增 `setUrlModifier` 操作和 `urlModifier/urlPostApplyModifier` 欄位 `LayerViewInfo`， `TemplateInfo`、和 `WatermarkInfo`.

已新增 `createDerivedAsset` 作業。 目前為 `ownerHandle` 必須參考影像資產，型別可以是 `AdjustedView` 或 `LayerView`.

已新增 `createTemplate` 作業。 呼叫以建立範本或浮水印資產。

IPS公司設定， `CompanySettings`，移轉至網站服務API。

已新增 `excludeByproducts` 篩選標幟至 `searchAssets` 作業。 將此標幟設定為true執行 `PSDlayer` 影像和PDF擷取的影像。

已新增 `getGenerationInfo` 作業。

已新增 `SystemMessage` 屬性名稱至 `getProperty` 作業。

修改部分資產型別字串常數，以符合對應的資產資訊欄位。

* WordDoc： Word
* ExcelDoc： Excel
* PowerPointDoc： PowerPoint
* RTFDoc： Rtf

修改批次作業的結果格式，以彙總成功、警告和錯誤。

已實作 `batchSetAssetMetadata` 批次中繼資料作業。

實作應用程式特定資料的支援。

實作布林值標幟的支援 `createTemplate`， `extendLayers`、和 `extractText` 用於上傳工作，以控制Photoshop的處理程式（類似於新增檔案上傳的變更）。

已實作 `setImageMaps` 和 `setZoomTargets` 作業。

已實作 `ViewerPreset` 作業。 可識別的型別包括：

* `VideoPlayer` （影片只會發佈這些檢視器）。
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

檢視器外觀元素支援兩個引數： `skinFg` 和 `skinBg`. 後端程式碼會執行維持回溯相容性所需的所有處理。

已實作 `getAssociatedAssets` 作業。

已新增 `ReprocessAssets` 允許重新處理先前上傳的主要來源檔案的工作型別，包括重新擷取PDF和重新最佳化影像。

已重新命名 `PropertySetType` 欄位型別至 `propertyType`. 此重新命名會影響 `createPropertySetType` 引數和 `getPropertySetType/getPropertySetTypes` 回應。

已實作 `batchSetImageFields` 支援設定影像使用者資料和其他可編輯影像欄位的作業。

47將fileSize欄位新增至各種資產資訊型別：

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

已實作 `getActivePublishContexts` 作業。 此操作會傳回具有指定公司之作用中發佈伺服器的發佈內容名稱陣列。 目前的發佈內容名稱為：

* `ImageServing`
* `ImageRendering`
* `Video`

已實作 `getSearchStrings` 作業。 它會傳回指定資產的搜尋字串陣列。

新增工作的地區設定引數，以及設定API作業地區設定的機制。 地區設定字串的格式應該是 `<language_code>[-<country_code>]`. 語言代碼是ISO-639所指定的小寫雙字母代碼，而選用的國家/地區代碼是ISO-3166所指定的大寫雙字母代碼。

將選用的地區設定引數新增至 `authHeader` 設定API作業地區設定的SOAP標頭。 如果此引數不存在，HTTP標頭 `Accept-Language` 已使用。 如果此標頭也不存在，則會使用IPS伺服器的預設地區設定。

新增強型別中繼資料欄位的get/set支援。

實作對gzip回應控制項的SOAP和HTTP標頭支援。

已新增 `gzipResponse` 標幟到 `authHeader`. 如果不存在，API會檢查HTTP `Accept-Encoding` 標頭。

新增對searchAssets的強型別中繼資料欄位條件支援。

* 對於所有欄位型別，值可透過字串比較運運算元( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* 對於布林值欄位， `boolVal` 可透過 `Equals` 操作。
* 對於Int欄位， `longVal` 可透過數值比較運運算元( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minLong/maxLong` 可透過數值範圍作業( `Between, NotBetween`)。
* 對於Float欄位， `doubleVal` 可透過數值比較運運算元( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minDouble/maxDouble` 可透過數值範圍作業( `Between, NotBetween`)。
* 對於日期欄位，您可以傳遞 `dateVal` 使用數值比較運運算元( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或您可以透過數值範圍作業( `Between, NotBetween`)。

已新增說明， `jobSubType`、和 `originalJobName` 欄位至 `JobLog` 型別。

* `originalJobName` 是工作名稱已提交至 `submitJob` （沒有任何唯一性尾碼或後續工作名稱）。
* `jobSubType` 僅供 `ImageServingPublishJob` 工作（其中為下列之一） `full`， `increment, fullwithsearch,` 或 `fulloverride`)。
* `description` 是適用於所有工作型別的空字串，但最終包含摘要工作資訊，例如上傳路徑。

此外，以下欄位不會同時包含於兩者 `getJobLogs` 和 `getJobLogDetails`. 在舊版中，它們僅適用於 `getJobLogDetails`.

* `endDate` （如果工作已完成）。
* `fileDuplicateCount` (之前一直 `0` 替換為 `getJobLogs`)
* `fileUpdateCount` (先前一直 `0` 替換為 `getJobLogs` 並包含在 `fileSuccessCount`；現在會分割成個別欄位)。

將assetHandle欄位新增至 `JobLogDetail` 型別。

新增選用說明引數至 `submitJob`. 傳遞此引數以便擷取 `getScheduledJobs`， `getActiveJobs`、和 `getJobLogs`.

已棄用SKU系統欄位。 如果欄位作為「 」傳入，則會忽略該欄位 `SystemFieldCondition` 至 `searchAssets`.

已新增 `excludeAssetTypeArray` 篩選至 `searchAssets`.

已新增 `MaskInfo` 輸入至 `Asset`.

已新增IPS管理的新資產型別：

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>资源类型 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS和PostScript檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>以.doc結尾之檔案的Microsoft® Word檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>以.xls結尾之檔案的Microsoft® Excel檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>以.ppt結尾之檔案的Microsoft® PowerPoint檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>以.rtf結尾的上傳檔案的RTF檔案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新增其他選項至 `UploadDirectoryJob` 和 `UploadUrlsJob` 獨立控制Postscript、Illustrator和PDF檔案的處理。 所有現有作業都會為三個處理管道的每個提供必要引數，以便它們能夠完全按照今天的方式運作。 原始 `PostScriptOptions` 區塊是用來設定Illustrator和EPS/PS檔案的處理作業。 您可以選擇提供特定的檔案選項區塊來指定處理。 變更清單包括：

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>字段 </p> </th> 
   <th colname="col2" class="entry"> <p>参数 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 點陣化 </span>（預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以指定的解析度和色域將EPS和PostScript檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化成影像時生效。 如果以這種方式定義原始檔案以覆蓋標誌，則會建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 无 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 點陣化 </span> （預設） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以指定的解析度和色域將檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>呈現的目標色彩空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>將檔案點陣化成影像時生效。 如果以這種方式定義原始檔案來建立重疊圖志，則建立透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 點陣化 </span> （預設） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>僅管理資產，上傳時不會建立任何衍生工具。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以指定的解析度和色域將檔案演算為影像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>點陣化解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>呈現的目標色彩空間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義在呈現後是否將多頁PDF合併到eCatalog中（預設為true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定義是否將PDF中的字詞擷取到DB以供稍後提供給搜尋伺服器（預設為false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您也可以從下列位置查詢： `getScheduledJobs`.

已修改 `webservice.gzip.response` 設定屬性以取得下列其中一個值：

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>不要gzip回應。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip回應僅在authHeader/gzipResponse為true時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip （如果authHeader/gzipResponse為true，或不存在gzipResponse標頭且HTTP Accept-Encoding標頭包含gzip）。 (默认). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>一律gzip回應，無論標頭值為何。 此值僅用於偵錯。 </p> </td> 
  </tr> 
 </tbody> 
</table>
