---
description: 允许重新处理以前上载的主文件的作业类型，包括重新翻录PDF和重新优化图像。
solution: Experience Manager
title: 重新处理资产作业
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

允许重新处理以前上载的主文件的作业类型，包括重新翻录PDF和重新优化图像。

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
   <td colname="col2"> <p><span class="codeph">类型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>资产句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>文件是否已标记为准备发布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>控制覆盖时是否保留现有资源的发布状态。 如果未设置，则使用公司默认设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>是否创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>控制任何现有裁切定义的保留。 默认为 true。</p> <p>如果您提供manualCropOptions参数和相应的值，则无论是否使用preserveCrop值，新值（不包括0,0，0,0）都会应用于资源。</p><p>如果您<i>未</i>提供manualCropOptions参数，则保留preserveCrop的值。 如果为true，则会保留现有的preserveCrop值；如果为false，则会删除preserveCrop值。</p><p>示例：</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手动裁切选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根据颜色自动裁切图像的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根据透明度从图像边缘去除空格。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将Photoshop文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将PostScript文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将PDF文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V媒体文件选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将Illustrator文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>可在上载过程中指定的选项。 该集会影响如何为上传管理颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>要应用于上载文件的自动生成集脚本的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>项目句柄的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname">电子邮件设置</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>电子邮件设置选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：boolean</span> </p> </td> 
   <td colname="col3"> <p>是否只上传文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>指向文件上传位置的URL。 </p> </td> 
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
   <td colname="col3"> <p>要在上传完成后运行的视频发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将InDesign文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> clokoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：挖空背景选项</span> </p> </td> 
   <td colname="col3"> <p>蒙版所选图像的背景。 这样，您就可以将它们叠加到其他图层中，并在主题图像之外具有透明度。 </p> <p>可选. </p> <p>请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local">挖空背景选项</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">类型：UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>允许您在创建优化的金字塔TIF文件时控制钝化蒙版设置的选项。 使用这些设置帮助提高图像锐度。 </p> <p>查看<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html?lang=zh-Hans"> UnsharpMaskOptions</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**备注**

`*CropOptions`的选项包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`的选项包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
