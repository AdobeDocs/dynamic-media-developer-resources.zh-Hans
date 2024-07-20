---
title: RipPdf作业
description: 表示现有PDF资源的进程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

表示现有PDF资源的进程。

>[!NOTE]
>
>此作业类型已弃用。 过渡到所有未来集成的`ReprocessAssetsJob`。

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
   <td colname="col2"> <p><span class="codeph">类型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>要翻录的PDF文件数组的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>确定是否要创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手动裁切选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>自动裁切选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>项目句柄的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname">电子邮件设置</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>电子邮件设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>文件上载到的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上载完成后要运行的图像服务发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上载完成后要运行的图像渲染发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>上传完成后要运行的视频发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将Adobe InDesign文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> clokoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：挖空背景选项</span> </p> </td> 
   <td colname="col3"> <p>蒙版所选图像的背景。 此功能允许您将其叠加到其他图层中，并使其在主题图像之外透明。 </p> <p>可选. </p> <p>请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local">挖空背景选项</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

`*CropOptions`的选项包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`的选项包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
