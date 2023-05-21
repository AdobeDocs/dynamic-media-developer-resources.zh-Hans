---
description: 資料夾階層中的物件或容器。
solution: Experience Manager
title: 資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 8%

---

# [!DNL Asset]{#asset}

資料夾階層中的物件或容器。

语法

## 参数 {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL acoInfo]</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL animatedGifInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AnimatedGifInfo</span> </td> 
   <td colname="col3"> 有關動畫GIF檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產控點。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetSetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cabinetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：封包資訊</span> </td> 
   <td colname="col3"> 封包資產型別的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL created]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 上傳資產的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL createUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 建立資產之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cssInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：CssInfo</span> </td> 
   <td colname="col3"> CSS檔案的詳細資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cuePointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL excelInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">傳回虛擬檔案名稱。 完整的虛擬檔案路徑為 <span class="codeph"> 資料夾</span>+<span class="codeph"> 檔案名稱</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL flashInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 包含資產的資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folderHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產上層資料夾的處理常式。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fontInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 文字：fontInfo</span> </td> 
   <td colname="col3"> 字型資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL iccProfileInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：IccProfileInfo</span> </td> 
   <td colname="col3"> ICC設定檔資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL illustratorInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：影像資訊</span> </td> 
   <td colname="col3"> 影像資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL inDesignInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL ipsImageUrl]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 代表資產縮圖檢視的相對URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL javascriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：JavascriptInfo</span> </td> 
   <td colname="col3"> JavaScript檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModified]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 上次修改資產的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModifyUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上次修改資產之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL layerViewInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：LayerViewInfo</span> </td> 
   <td colname="col3"> 圖層檢視資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masterVideoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL metadataArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：MetadataArray</span> </td> 
   <td colname="col3"> 與資產相關聯的中繼資料值陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL name]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfSettingsInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF設定資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL permissions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL postScriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL powerPointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL premiereExpressInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL projects]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 專案名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL psdInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定旗標以指出是否應該發佈資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL renderSceneInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：RenderSceneInfo</span> </td> 
   <td colname="col3"> 演算場景資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL rtfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL subType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">支援子型別值的一般資產子型別(例如， <span class="codeph"> 資產集</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL svgInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：SvgInfo</span> </td> 
   <td colname="col3"> SVG資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL swcInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：SwcInfo</span> </td> 
   <td colname="col3"> SWC資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL templateInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：TemplateInfo</span> </td> 
   <td colname="col3"> 範本資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL trashState]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指出資產是在垃圾桶中還是即時狀態（請參閱「垃圾桶狀態」以瞭解值）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL type]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">资源类型. 另請參閱 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 資產型別</a> 以取得值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoCaptionInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>視訊註解資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> <p>視訊資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerPresetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：檢視器預設集資訊</span> </td> 
   <td colname="col3"> 檢視器預設集資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerSwfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：檢視器SwfInfo</span> </td> 
   <td colname="col3"> 檢視器軟體資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL vignetteInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VignetteInfo</span> </td> 
   <td colname="col3"> 暈映資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL watermarkInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：WatermarkInfo</span> </td> 
   <td colname="col3"> 浮水印資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL windowCoveringInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：視窗涵蓋範圍資訊</span> </td> 
   <td colname="col3"> 涵蓋資產的視窗屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL wordInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL xmlInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：XmlInfo</span> </td> 
   <td colname="col3"> XML資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：XslInfo</span> </td> 
   <td colname="col3"> XSL資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
