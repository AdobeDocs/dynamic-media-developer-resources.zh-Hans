---
description: 定期从指定的服务器目录上载文件。
seo-description: 定期从指定的服务器目录上载文件。
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

定期从指定的服务器目录上载文件。

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
   <td colname="col1"> <span class="codeph"> 自 <span class="varname"> 动颜色选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AutoColorOptions</span> </td> 
   <td colname="col3"> <p>自动图像裁剪选项（基于颜色）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>要应用于已上载文件的自动设置生成脚本的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>根据透明度从图像边缘删除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 颜 <span class="varname"> 色管理选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>可在上传过程中指定的选项。 该设置会影响为上传管理颜色的方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 创 <span class="varname"> 建蒙版</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>上传时是否创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> destFolder <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>文件的IPS文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 电子 <span class="varname"> 邮件设置</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>选择电子邮件设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustrator选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>用于将Illustrator文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 包含子 <span class="varname"> 文件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>上传时是否包含子文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesign选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：InDesignOptions</span> </td> 
   <td colname="col3"> <p>用于将InDesign文件上传到服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 挖 <span class="varname"> 空背景</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>遮住所选图像的背景。 这样，您就可以在主题图像外部以透明方式将其叠加到其他图层中。 </p> <p>可选。 </p> <p>请参 <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 阅KnockoutBackgroundOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 手 <span class="varname"> 动裁剪选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>手动图像裁剪选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 媒 <span class="varname"> 体选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MediaOptions</span> </td> 
   <td colname="col3"> <p>用于从视频中设置缩略图的选项。 </p> <p>请参阅 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 媒体选项</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆盖</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>文件上传覆盖选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PDFOptions</span> </td> 
   <td colname="col3"> <p>用于将PDF文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> photoshop <span class="varname"> 选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>用于将Photoshop文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>文件上传目标的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Job </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>上传完成后运行的图像渲染发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>上传完成后运行的图像服务发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是否仅上传文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>用于将Post Script文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VideoPublishJob</span> </td> 
   <td colname="col3"> <p>上传完成后运行的视频发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 保 <span class="varname"> 留裁剪</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>控制任何现有裁切定义的保留。 默认值为true。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 保 <span class="varname"> 留PublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>控制在覆盖时是否保留现有资产的发布状态。 如果未设置，则使用公司默认设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> processMetadataFiles <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>是否为此作业处理单独的元数据XML文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>项目句柄的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 就 <span class="varname"> 绪发布</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>确定文件是否已标记为可发布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 服 <span class="varname"> 务器目录</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>源上传目录。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>使用这些可选设置提取和处理已上载TAR/ZIP文件的内容。 </p> <p>请参 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 阅UnCompressOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> USMsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：USMsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>用于在创建优化金字塔TIF文件时控制USM锐化设置的选项。 使用这些设置有助于提高图像锐度。 </p> <p>请参 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> 阅USMsharpMaskOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>上载作业中所有内容的附加元数据选项 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 说明 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

对 `CropOptions`于，您只能选择以下选项之一：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

对 `PublishJob`于，您只能选择以下选项之一：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

