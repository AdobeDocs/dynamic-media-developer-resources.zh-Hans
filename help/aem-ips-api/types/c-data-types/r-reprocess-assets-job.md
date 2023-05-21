---
description: 允許重新處理先前上傳之主要檔案的工作型別，包括重新擷取PDF和重新最佳化影像。
solution: Experience Manager
title: 重新處理資產工作
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 5%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

允許重新處理先前上傳之主要檔案的工作型別，包括重新擷取PDF和重新最佳化影像。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>資產控點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>檔案是否已標示為可供發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制覆寫時是否保留現有資產的發佈狀態。 如果未設定，則會使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否要建立遮色片。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制任何現有裁切定義的保留。 默认为 true。</p> <p>如果您提供manualCropOptions引數和對應的值，則無論是否有preserveCrop值，都會將新值（不包括0,0，0,0）套用至資產。</p><p>如果您有 <i>not</i> 提供manualCropOptions引數，保留preserveCrop的值。 如果為true，則會保留現有的preserveCrop值；如果為false，則會移除preserveCrop值。</p><p>示例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據顏色自動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根據透明度，移除影像邊緣的空白區域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>將Photoshop檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>上傳PostScript檔案至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>將PDF檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V媒體檔案選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>將Illustrator檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>您可在上傳期間指定的選項。 此集會影響如何管理上傳的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>要套用至上傳檔案的自動集合產生指令碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>專案控點的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子郵件設定的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFile</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否只上傳檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>檔案上傳位置的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postimageservingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>影像伺服發佈工作之工作詳細資訊將在上傳完成後執行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後要執行的影像演算發佈工作的工作詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postvideopublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上傳完成後要執行的視訊發佈工作之工作詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>將InDesign檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 去底色背景</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：去底色背景選項</span> </p> </td> 
   <td colname="col3"> <p>遮色所選影像的背景。 如此一來，您就可以用主題影像之外的透明度，將之覆蓋在其他圖層上。 </p> <p>可选. </p> <p>另請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景選項</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：不銳利化遮色片選項</span> </p> </td> 
   <td colname="col3"> <p>可讓您在建立最佳化的金字塔TIF檔案時控制遮色片銳利化調整設定的選項。 使用這些設定來協助改善影像銳利度。 </p> <p>另請參閱 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> 不銳利化遮色片選項</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**说明**

選擇 `*CropOptions` 包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選擇 `*PublishJob` 包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
