---
description: 使用getActiveJobs跟踪桌面上传。
seo-description: 使用getActiveJobs跟踪桌面上传。
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Dynamic Media Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 10%

---


# UploadPostJob{#uploadpostjob}

使用getActiveJobs跟踪桌面上传。

另请参阅[通过HTTP POST将资产上传到上传……](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d)。

>[!NOTE]
>
>上传作业的所有POST请求必须源自相同的IP地址。

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
   <td colname="col2"> <span class="codeph"> 类型：AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>基于颜色的图像自动裁剪选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>要应用于已上载文件的自动设置生成脚本的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根据透明度从图像边缘删除空白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上传过程中可以指定的选项。 该设置会影响上传颜色的管理方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>是否创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>电子邮件设置选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：InDesignOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于将InDesign文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：IllustratorOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>将Illustrator文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 挖空背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoudBackgroundOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>遮住所选图像的背景。 这样，您就可以在主题图像外部以透明方式将其叠加到其他图层中。 可选。 </p> <p>请参阅<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>手动裁剪图像的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MediaOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于从视频中设置缩略图的选项。 </p> <p>请参阅<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆盖</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是</p> </td> 
   <td colname="col4"> <p>上传时是否覆盖文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf选项</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PDFOptions</span> </td> 
   <td colname="col3"> <p>否</p> </td> 
   <td colname="col4"> <p>将PDF文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>将Photoshop文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上载文件的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于将Post Script文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>控制任何现有裁剪定义的保留。 默认为 true。</p> <p>如果您提供manualCropOptions参数和相应值，则无论preserveCrop值如何，新值（不包括0,0,0,0）都将应用于资产。</p><p>如果<i>不</i>提供manualCropOptions参数，则保留Crop的值。 并且，如果为true，则保留现有的preserveCrop值；如果为false，则删除preserveCrop值。</p><p>示例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt; 190&lt;/left&gt;<br />    &lt;right&gt; 310&lt;/right&gt;<br />    &lt;top&gt; 160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>控制在覆盖时是否保留现有资产的发布状态。 如果未设置，则使用公司默认设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>项目句柄的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>文件是否已标记为可发布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>使用这些可选设置提取并处理已上传的TAR/ZIP文件的内容。 </p> <p>请参阅<a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:USMsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于在创建优化的金字塔TIF文件时控制USM锐化设置的选项。 使用这些设置有助于提高图像锐度。 </p> <p>请参阅<a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UsmarpMaskOptions</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上载作业中所有内容的附加元数据选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

