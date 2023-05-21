---
description: 使用getActiveJobs追蹤案頭上傳。
solution: Experience Manager
title: UploadpostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# [!DNL UploadPostJob]{#uploadpostjob}

使用getActiveJobs追蹤案頭上傳。

另請參閱 [正在透過HTTP POST將資產上傳至上傳……](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>上傳工作的所有POST請求都必須來自相同的IP位址。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需? </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根據顏色自動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>要套用至上傳檔案的自動集合產生指令碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根據透明度，移除影像邊緣的空白區域。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>您可在上傳期間指定的選項。 此集會影響如何管理上傳的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>是否要建立遮色片。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>選擇電子郵件設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：InDesignOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將InDesign檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將Illustrator檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 去底色背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：去底色背景選項</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>遮色所選影像的背景。 如此一來，您就可以用主題影像之外的透明度，將之覆蓋在其他圖層上。 可选. </p> <p>另請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景選項</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>手動裁切影像的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：MediaOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可讓您從視訊設定縮圖影像的選項。 </p> <p>另請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆寫</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是</p> </td> 
   <td colname="col4"> <p>上傳時是否覆寫檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PDFOptions</span> </td> 
   <td colname="col3"> <p>否</p> </td> 
   <td colname="col4"> <p>將PDF檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將Photoshop檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上傳檔案的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>將後置指令碼檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>控制任何現有裁切定義的保留。 默认为 true。</p> <p>如果您提供manualCropOptions引數和對應的值，則無論是否有preserveCrop值，都會將新值（不包括0,0，0,0）套用至資產。</p><p>如果您有 <i>not</i> 提供manualCropOptions引數，保留preserveCrop的值。 如果為true，則會保留現有的preserveCrop值；如果為false，則會移除preserveCrop值。</p><p>示例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>控制覆寫時是否保留現有資產的發佈狀態。 如果未設定，則會使用公司預設設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>專案控點的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>檔案是否已標示為可供發佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uncompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>使用這些選擇性設定來擷取及處理已上傳TAR/ZIP檔案的內容。 </p> <p>另請參閱 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：不銳利化遮色片選項</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可讓您在建立最佳化的金字塔TIF檔案時控制遮色片銳利化調整設定的選項。 使用這些設定來協助改善影像銳利度。 </p> <p>另請參閱 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> 不銳利化遮色片選項</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>適用於上傳工作中一切的額外中繼資料選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>
