---
description: 定期從指定的伺服器目錄上傳檔案。
solution: Experience Manager
title: UploadDirectory作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 7%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

定期從指定的伺服器目錄上傳檔案。

语法

## 参数 {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoColorOptions</span> </td> 
   <td colname="col3"> <p>自動影像裁切選項（根據顏色）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>要套用至上傳檔案的自動集合產生指令碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>根據透明度，移除影像邊緣的空白區域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>您可在上傳期間指定的選項。 此集會影響如何管理上傳的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>上傳時是否要建立遮罩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>檔案的IPS資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>選擇電子郵件設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>將Illustrator檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>上傳時是否包含子資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：InDesignOptions</span> </td> 
   <td colname="col3"> <p>將InDesign檔案上傳至伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 去底色背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：去底色背景選項</span> </td> 
   <td colname="col3"> <p>遮色所選影像的背景。 如此一來，您就可以用主題影像之外的透明度，將之覆蓋在其他圖層上。 </p> <p>可选. </p> <p>另請參閱 <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景選項</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>手動影像裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：MediaOptions</span> </td> 
   <td colname="col3"> <p>可讓您從視訊設定縮圖影像的選項。 </p> <p>另請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆寫</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>檔案上傳覆寫選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PDFOptions</span> </td> 
   <td colname="col3"> <p>將PDF檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>將Photoshop檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>檔案上傳目的地的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>工作 </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>上傳完成後執行的影像演算發佈工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postimageservingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>上傳完成後執行的影像伺服發佈工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFile</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是否只上傳檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>上傳Post Script檔案至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postvideopublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VideoPublishJob</span> </td> 
   <td colname="col3"> <p>上傳完成後執行的視訊發佈工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>控制任何現有裁切定義的保留。 預設為true。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>控制覆寫時是否保留現有資產的發佈狀態。 如果未設定，則會使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>是否為此工作處理個別的中繼資料XML檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3"> <p>專案控點的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>決定檔案是否標示為可發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>來源上傳目錄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uncompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>使用這些選擇性設定來擷取及處理已上傳TAR/ZIP檔案的內容。 </p> <p>另請參閱 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：不銳利化遮色片選項</span> </td> 
   <td colname="col3"> <p>可讓您在建立最佳化的金字塔TIF檔案時控制遮色片銳利化調整設定的選項。 使用這些設定來協助改善影像銳利度。 </p> <p>另請參閱 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> 不銳利化遮色片選項</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>適用於上傳工作中一切的額外中繼資料選項 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

對象 `CropOptions`，您只能選擇下列其中一項：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

對象 `PublishJob`，您只能選擇下列其中一項：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
