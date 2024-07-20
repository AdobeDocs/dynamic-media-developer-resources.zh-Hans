---
description: 从要获取文件的位置上传URL。
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---

# [!DNL UploadUrlsJob]{#uploadurlsjob}

从要获取文件的位置上传URL。

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
   <td colname="col2"> <span class="codeph">类型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 根据颜色自动裁切图像的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：AutoSetCreationOptions</span> </td> 
   <td colname="col3"> 要应用于上载文件的自动生成集脚本的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 根据透明度从图像边缘去除空格。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 是否创建蒙版。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：ColorManagementOptions</span> </td> 
   <td colname="col3"> 可在上载过程中指定的选项。 该集会影响如何为上传管理颜色。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">电子邮件设置</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 电子邮件设置的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：IllustratorOptions</span> </td> 
   <td colname="col3"> 用于将Illustrator文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：InDesignOptions</span> </td> 
   <td colname="col3"> 用于将InDesign文件上传到服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> clokoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：挖空背景选项</span> </td> 
   <td colname="col3">蒙版所选图像的背景。 这样，您就可以将它们叠加到其他图层中，并在主题图像之外具有透明度。 可选。 请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> ClokoutBackgroundOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：ManualCropOptions</span> </td> 
   <td colname="col3"> 手动裁切图像的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：MediaOptions</span> </td> 
   <td colname="col3">允许您从视频设置缩略图图像的选项。 请参阅<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3">返回作业中提交的URL数。 由<a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a>和<a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">覆盖</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 上传时是否覆盖文件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：PDFOptions</span> </td> 
   <td colname="col3"> 用于将PDF文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：PhotoshopOptions</span> </td> 
   <td colname="col3"> 用于将Photoshop文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 正在上传文件的URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 上载完成后运行的图像渲染发布作业的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 所有介质选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：PostScriptOptions</span> </td> 
   <td colname="col3"> 用于将后脚本文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：VideoPublishJob</span> </td> 
   <td colname="col3"> 上传完成后运行的视频发布作业的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 控制任何现有裁切定义的保留。 默认为true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 控制覆盖时是否保留现有资源的发布状态。 如果未设置，则使用公司默认设置。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：HandleArray</span> </td> 
   <td colname="col3"> 项目句柄数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 文件是否已标记为准备发布。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：UnCompressOptions</span> </td> 
   <td colname="col3">使用这些可选设置提取并处理已上传TAR/ZIP文件的内容。 请参阅<a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：UnsharpMaskOptions</span> </td> 
   <td colname="col3">允许您在创建优化的金字塔TIF文件时控制钝化蒙版设置的选项。 使用这些设置帮助提高图像锐度。 查看<a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：UrlArray</span> </td> 
   <td colname="col3"> 要上载的URL数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>上载作业中所有内容的附加元数据选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

对于`CropOptions`，您只能选择下列选项之一：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

对于`PublishJob`，您只能选择下列选项之一：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
