---
description: 作业类型允许重新处理以前上传的主文件，包括重新翻录PDF和重新优化图像。
seo-description: 作业类型允许重新处理以前上传的主文件，包括重新翻录PDF和重新优化图像。
seo-title: 重新处理AssetsJob
solution: Experience Manager
title: 重新处理AssetsJob
topic: Dynamic Media Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 5%

---


# ReprocessAssetsJob{#reprocessassetsjob}

作业类型允许重新处理以前上传的主文件，包括重新翻录PDF和重新优化图像。

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
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>资产句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>文件是否已标记为可发布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制在覆盖时是否保留现有资产的发布状态。 如果未设置，则使用公司默认设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>控制任何现有裁剪定义的保留。 默认为 true。</p> <p>如果您提供manualCropOptions参数和相应值，则无论preserveCrop值如何，新值（不包括0,0,0,0）都将应用于资产。</p><p>如果<i>不</i>提供manualCropOptions参数，则保留Crop的值。 并且，如果为true，则保留现有的preserveCrop值；如果为false，则删除preserveCrop值。</p><p>示例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt; 190&lt;/left&gt;<br />    &lt;right&gt; 310&lt;/right&gt;<br />    &lt;top&gt; 160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>手动裁剪选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>基于颜色的图像自动裁剪选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>根据透明度从图像边缘删除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>将Photoshop文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将PostScript文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdf选项</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>将PDF文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V媒体文件选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>将Illustrator文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>上传过程中可以指定的选项。 该设置会影响上传颜色的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>要应用于已上载文件的自动设置生成脚本的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>一组项目句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>电子邮件设置选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>是否仅上载文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>文件上传位置的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>要在上载完成后运行的图像服务发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>要在上载完成后运行的图像渲染发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>要在上载完成后运行的视频发布作业的作业详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>用于将InDesign文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 挖空背景</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:KnockoudBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>遮住所选图像的背景。 这样，您就可以在主题图像外部以透明方式将其叠加到其他图层中。 </p> <p>可选。 </p> <p>请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> usmsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:USMsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>用于在创建优化的金字塔TIF文件时控制USM锐化设置的选项。 使用这些设置有助于提高图像锐度。 </p> <p>请参阅<a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UsmarpMaskOptions</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**说明**

`*CropOptions`的选项包括：

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`*PublishJob`的选项包括：

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

