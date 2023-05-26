---
description: 使用getActiveJobs跟踪桌面上载。
solution: Experience Manager
title: UploadPost作业
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# [!DNL UploadPostJob]{#uploadpostjob}

使用getActiveJobs跟踪桌面上载。

另请参阅 [正在通过HTTP POST将资产上传到上传……](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>上载作业的所有POST请求必须源自相同的IP地址。

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
   <td colname="col4"> <p>根据颜色自动裁切图像的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetcreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>要应用于上载文件的自动生成集脚本数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>根据透明度从图像边缘去除空格。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：颜色管理选项</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可在上载期间指定的选项。 该集会影响如何为上传管理颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>是否创建蒙版。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 电子邮件设置</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>电子邮件设置的选择。 </p> </td> 
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
   <td colname="col4"> <p>用于将Illustrator文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 挖空背景</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：去底色背景选项</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>蒙版所选图像的背景。 这样，您就可以使用主题图像以外的透明度，将其叠加到其他图层中。 可选. </p> <p>参见<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 去底色背景选项</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ManualCropOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>手动裁切图像的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MediaOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>允许您从视频设置缩略图图像的选项。 </p> <p>参见 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 媒体选项</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 覆盖</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>是</p> </td> 
   <td colname="col4"> <p>上传时是否覆盖文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PDFOptions</span> </td> 
   <td colname="col3"> <p>否</p> </td> 
   <td colname="col4"> <p>用于将PDF文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于将Photoshop文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上传文件的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：PostScriptOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于将后脚本文件上传到图像服务器的选项。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>控制任何现有裁切定义的保留。 默认为 true。</p> <p>如果您提供manualCropOptions参数和相应的值，则无论是否使用preserveCrop值，新值（不包括0,0，0,0）都会应用于资源。</p><p>如果您这样做 <i>非</i> 提供manualCropOptions参数，保留preserveCrop的值。 如果为true，则会保留现有的preserveCrop值；如果为false，则会删除preserveCrop值。</p><p>示例：</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>控制覆盖时是否保留现有资源的发布状态。 如果未设置，则使用公司默认设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandlearray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：HandleArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>项目句柄数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>是</b> </p> </td> 
   <td colname="col4"> <p>文件是否标记为可发布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uncompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：UnCompressOptions</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>使用这些可选设置提取并处理上传的TAR/ZIP文件的内容。 </p> <p>参见 <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：USM选项</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>允许您在创建优化的金字塔TIF文件时控制钝化蒙版设置的选项。 使用这些设置有助于提高图像清晰度。 </p> <p>参见 <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>上载作业中所有内容的附加元数据选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>
