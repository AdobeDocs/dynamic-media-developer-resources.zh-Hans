---
description: 從您要取得檔案的位置上傳URL。
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 5%

---

# [!DNL UploadUrlsJob]{#uploadurlsjob}

從您要取得檔案的位置上傳URL。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 根據顏色自動裁切影像的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoSetCreationOptions</span> </td> 
   <td colname="col3"> 要套用至上傳檔案的自動集合產生指令碼陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 根據透明度，移除影像邊緣的空白區域。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否要建立遮色片。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ColorManagementOptions</span> </td> 
   <td colname="col3"> 您可在上傳期間指定的選項。 此集會影響如何管理上傳的顏色。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選擇電子郵件設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：IllustratorOptions</span> </td> 
   <td colname="col3"> 將Illustrator檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：InDesignOptions</span> </td> 
   <td colname="col3"> 將InDesign檔案上傳至伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 去底色背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：去底色背景選項</span> </td> 
   <td colname="col3">遮色所選影像的背景。 如此一來，您就可以用主題影像之外的透明度，將之覆蓋在其他圖層上。 可选. 另請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景選項</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ManualCropOptions</span> </td> 
   <td colname="col3"> 手動裁切影像的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：MediaOptions</span> </td> 
   <td colname="col3">可讓您從視訊設定縮圖影像的選項。 另請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">傳回工作中提交的URL數量。 使用者 <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> 和 <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆寫</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 上傳時是否覆寫檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PDFOptions</span> </td> 
   <td colname="col3"> 將PDF檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PhotoshopOptions</span> </td> 
   <td colname="col3"> 將Photoshop檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上傳檔案的URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 上傳完成後執行的影像演算發佈工作的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postimageservingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 所有媒體選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PostScriptOptions</span> </td> 
   <td colname="col3"> 將後置指令碼檔案上傳至影像伺服器的選項。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postvideopublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VideoPublishJob</span> </td> 
   <td colname="col3"> 上傳完成後執行的視訊發佈工作的詳細資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制任何現有裁切定義的保留。 預設為true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制覆寫時是否保留現有資產的發佈狀態。 如果未設定，則會使用公司預設設定。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3"> 專案控點的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 檔案是否已標示為可供發佈。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uncompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UnCompressOptions</span> </td> 
   <td colname="col3">使用這些選擇性設定來擷取及處理已上傳TAR/ZIP檔案的內容。 另請參閱 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：不銳利化遮色片選項</span> </td> 
   <td colname="col3">可讓您在建立最佳化的金字塔TIF檔案時控制遮色片銳利化調整設定的選項。 使用這些設定來協助改善影像銳利度。 另請參閱 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> 不銳利化遮色片選項</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：UrlArray</span> </td> 
   <td colname="col3"> 您要上傳的URL陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>適用於上傳工作中一切的額外中繼資料選項。 </p> </td> 
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
