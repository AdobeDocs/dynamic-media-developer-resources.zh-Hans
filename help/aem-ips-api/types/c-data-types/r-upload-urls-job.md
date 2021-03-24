---
description: 从要获取文件的位置上载URL。
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 5%

---


# UploadUrlsJob{#uploadurlsjob}

从要获取文件的位置上载URL。

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
   <td colname="col2"> <span class="codeph"> 类型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> 用于自动裁剪基于颜色的图像的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> 要应用于已上载文件的自动设置生成脚本的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 根据透明度从图像边缘删除空白。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否创建蒙版。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> 可在上载过程中指定的选项。 该设置会影响对上载的颜色的管理方式。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 选择电子邮件设置。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Illustrator选项</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：IllustratorOptions</span> </td> 
   <td colname="col3"> 用于将Illustrator文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：InDesignOptions</span> </td> 
   <td colname="col3"> 用于将InDesign文件上载到服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 挖空背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">遮住所选图像的背景。 这样，您就可以在主题图像外部以透明方式将它们叠加到其他图层中。 可选。请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> 手动裁剪图像的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MediaOptions</span> </td> 
   <td colname="col3">用于从视频中设置缩略图的选项。 请参阅<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">返回作业中提交的URL数。 由<a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a>和<a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆盖</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 上载时是否覆盖文件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf选项</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PDFOptions</span> </td> 
   <td colname="col3"> 用于将PDF文件上载到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PhotoshopOptions</span> </td> 
   <td colname="col3"> 用于将Photoshop文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上载文件的URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 上载完成后运行的图像渲染发布作业的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 所有媒体选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PostScriptOptions</span> </td> 
   <td colname="col3"> 用于将Post Script文件上传到图像服务器的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VideoPublishJob</span> </td> 
   <td colname="col3"> 上传完成后运行的视频发布作业的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制任何现有裁剪定义的保留。 默认为true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 控制在覆盖时是否保留现有资源的发布状态。 如果未设置，则使用公司默认设置。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> 项目句柄数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 文件是否已标记为可发布。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3">使用这些可选设置提取和处理已上载的TAR/ZIP文件的内容。 请参阅<a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：USMsharpMaskOptions</span> </td> 
   <td colname="col3">用于在创建优化金字塔TIF文件时控制USM锐化设置的选项。 使用这些设置有助于提高图像锐度。 请参阅<a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UsmarpMaskOptions</a>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> 要上传的URL数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>上载作业中所有内容的附加元数据选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

对于`CropOptions`，您只能选择以下选项之一：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

对于`PublishJob`，您只能选择以下选项之一：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

