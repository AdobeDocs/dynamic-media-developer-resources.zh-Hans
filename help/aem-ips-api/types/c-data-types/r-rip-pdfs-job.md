---
description: 重新擷取現有PDF資產的程式。
solution: Experience Manager
title: RipPdfJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 5%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

重新擷取現有PDF資產的程式。

>[!NOTE]
>
>此工作型別已過時。 轉換至 `ReprocessAssetsJob` 用於所有未來的整合。

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>要擷取的PDF檔案陣列的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>決定是否要建立遮色片。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手動裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>自動裁切選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>專案控點的陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>電子郵件設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>檔案上傳目標的URL。 </p> </td> 
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
   <td colname="col3"> <p>將Adobe InDesign檔案上傳至影像伺服器的選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 去底色背景</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：去底色背景選項</span> </p> </td> 
   <td colname="col3"> <p>遮色所選影像的背景。 如此一來，您就可以用主題影像之外的透明度，將之覆蓋在其他圖層上。 </p> <p>可选. </p> <p>另請參閱<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景選項</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

選擇 `*CropOptions` 包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

選擇 `*PublishJob` 包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
