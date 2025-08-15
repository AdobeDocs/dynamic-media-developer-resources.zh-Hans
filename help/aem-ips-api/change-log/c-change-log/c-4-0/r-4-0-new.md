---
title: 新增和变更
description: 介绍IPS API v4.0的新更改和已实施的更改。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# 新增和变更{#new-additions-and-changes}

介绍IPS API v4.0的新更改和已实施的更改。

使用单独的WSDL和架构命名空间并排实施的API版本。

* 早期API版本： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

已添加`PostScriptOptions/alpha`字段。

已为`VideoRootUrl`操作添加`SwfRootUrl`和`getProperty`属性。

已将可选`appName`和`appVersion`参数添加到`authHeader`以跟踪调用应用程序。 已将日志记录添加到`ipsApiService.log`。

向WSDL生成Servlet添加了可选的`serviceUrl`参数。 此参数对于调试代理很有用。 例如： `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已实施`getZipEntries`操作。

已实施搜索范围并键入系统字段条件的比较值。

添加了`'Asset'`资源类型字符串常量，主要是为了允许跨资源元数据字段。

已为`trashState`实施`searchAssets`参数。

已实施`getAssetPublishHistory`操作。

添加了可选的`faultHttpStatusCode`SOAP标头，以便在Flex中启用错误处理。 对于Flex，请使用`<faultHttpStatusCode>200</faultHttpStatusCode>`。 错误响应的默认状态代码为`500 (Internal Server Error)`。

添加了从垃圾桶中还原资源以及从垃圾桶中还原空资源的操作。

实施了CRUD操作。

已将启用的标志添加到`ImageMap`类型和`saveImageMap`操作。

添加了对优化剩余文件作业的支持。

添加了`setAssetsPublishState`以进行批量发布状态更新。

已添加`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`。

已弃用`saveMetadataField`操作以支持新的`createMetadataField`和`updateMetadataField`操作。

已实施`deleteAssetsParam`批次删除操作。

已实施`moveAssetsParam`批次移动操作。

已实施`deleteMetadataField`操作。

已实施`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`操作。

已实现`getAssetCounts`。

添加了对`setImageSetMembers`的支持，以便在`RenderSet`资源中包含`ImageSet`个成员。

添加了`replaceImage`操作。

添加了`copyImage`操作。

已为`setUrlModifier`、`urlModifier/urlPostApplyModifier`和`LayerViewInfo`添加`TemplateInfo`操作和`WatermarkInfo`字段。

添加了`createDerivedAsset`操作。 当前，`ownerHandle`必须引用图像资源，并且类型可以是`AdjustedView`或`LayerView`。

添加了`createTemplate`操作。 调用以创建模板或水印资产。

IPS公司设置`CompanySettings`已移植到Web服务API。

已将`excludeByproducts`筛选器标志添加到`searchAssets`操作。 将此标记设置为true可运行`PSDlayer`个图像和PDF翻录的图像。

添加了`getGenerationInfo`操作。

已将`SystemMessage`属性名称添加到`getProperty`操作。

修改了一些资源类型字符串常量，以匹配相应的资源信息字段。

* WordDoc： Word
* ExcelDoc： Excel
* PowerPointDoc： PowerPoint
* RTFDoc： Rtf

修改了批处理操作的结果格式，以汇总成功、警告和错误。

已实施`batchSetAssetMetadata`批处理元数据操作。

为应用程序特定的数据实施了支持。

为上载作业实施了对`createTemplate`、`extendLayers`和`extractText`的布尔标志的支持，以控制Photoshop处理的过程（与添加文件上载的更改类似）。

已实施`setImageMaps`和`setZoomTargets`操作。

已实施`ViewerPreset`操作。 可识别的类型包括：

* `VideoPlayer` （视频仅发布这些查看器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

查看器外观支持两个参数： `skinFg`和`skinBg`。 后端代码执行保持向后兼容性所需的所有处理。

已实施`getAssociatedAssets`操作。

添加了`ReprocessAssets`作业类型，以允许重新处理以前上载的主源文件，包括重新翻录PDF和重新优化图像。

已将`PropertySetType`字段类型重命名为`propertyType`。 此重命名会影响`createPropertySetType`参数和`getPropertySetType/getPropertySetTypes`响应。

已实施`batchSetImageFields`操作以支持设置图像用户数据和其他可编辑的图像字段。

47已将fileSize字段添加到各种资源信息类型：

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

已实施`getActivePublishContexts`操作。 此操作返回具有指定公司的活动发布服务器的发布上下文名称数组。 当前发布上下文名称为：

* `ImageServing`
* `ImageRendering`
* `Video`

已实施`getSearchStrings`操作。 它会返回给定资源的搜索字符串数组。

为作业添加了区域设置参数，并增加了设置API操作区域设置的机制。 区域设置字符串的格式应为`<language_code>[-<country_code>]`。 语言代码是由ISO-639指定的小写形式的双字母代码，而可选国家/地区代码是由ISO-3166指定的大写形式的双字母代码。

向`authHeader` SOAP标头添加了可选的区域设置参数，以设置API操作的区域设置。 如果此参数不存在，则使用HTTP标头`Accept-Language`。 如果此标头也不存在，则使用IPS服务器的默认区域设置。

为强类型元数据字段添加了get/set支持。

为gzip响应控制实施了SOAP和HTTP标头支持。

已将`gzipResponse`标志添加到`authHeader`。 如果不存在，则API会检查HTTP `Accept-Encoding`标头。

添加了对强类型元数据字段条件的searchAssets的支持。

* 对于所有字段类型，可以使用字符串比较运算符(`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)传递值
* 对于布尔字段，可以使用`boolVal`操作传递`Equals`。
* 对于Int字段，可以使用数字比较运算符(`longVal`)传递`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或者可以使用数字范围运算(`minLong/maxLong`)传递`Between, NotBetween`。
* 对于Float字段，可以使用数字比较运算符(`doubleVal`)传递`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或者可以使用数字范围运算(`minDouble/maxDouble`)传递`Between, NotBetween`。
* 对于日期字段，您可以通过数字比较运算符(`dateVal`)传递`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`，或者您可以通过数字范围运算(`Between, NotBetween`)传递minDate/maxDate。

已将描述`jobSubType`和`originalJobName`字段添加到`JobLog`类型。

* `originalJobName`是提交给`submitJob`的作业名称（没有任何唯一性后缀或后续作业名称）。
* `jobSubType`仅由`ImageServingPublishJob`个作业使用（其中是`full`、`increment, fullwithsearch,`或`fulloverride`之一）。
* `description`是所有作业类型的空字符串，但最终包含摘要作业信息，如上载路径。

此外，以下字段未同时包含在`getJobLogs`和`getJobLogDetails`中。 在以前的版本中，它们仅在`getJobLogDetails`中可用。

* `endDate` （如果作业已完成）。
* `fileDuplicateCount` （以前它始终为`0`，带有`getJobLogs`）
* `fileUpdateCount` （以前始终为`0`，带有`getJobLogs`，并包含在`fileSuccessCount`中；现在它被拆分为单独的字段）。

已将assetHandle字段添加到`JobLogDetail`类型。

向`submitJob`添加了可选描述参数。 传递此参数以在`getScheduledJobs`、`getActiveJobs`和`getJobLogs`中进行检索。

已弃用SKU系统字段。 如果字段作为`SystemFieldCondition`传递到`searchAssets`，则忽略该字段。

已将`excludeAssetTypeArray`筛选器添加到`searchAssets`。

已将`MaskInfo`类型添加到`Asset`。

添加了可由IPS管理的新资产类型：

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>资源类型 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS和PostScript文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word文档，用于以.doc结尾的文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>以.xls结尾的文件对应的Microsoft® Excel文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>以.ppt结尾的文件的Microsoft® PowerPoint文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>以.rtf结尾的上传文件的RTF文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

向`UploadDirectoryJob`和`UploadUrlsJob`添加了其他选项，用于控制独立处理Postscript、Illustrator和PDF文件。 所有现有作业都为三条处理管道中的每条管道提供必要参数，以便它们与今天完全相同。 原始`PostScriptOptions`块用于设置Illustrator和EPS/PS文件的处理。 或者，可以提供特定的文件选项块来指定处理。 更改列表包括：

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>字段 </p> </th> 
   <th colname="col2" class="entry"> <p>参数 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph">无</span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph">栅格化</span>（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>仅管理资产，上传时不会创建任何衍生工具。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>按照规定的分辨率和色彩空间将EPS和PostScript文件渲染到图像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布尔值&gt; </span> </p> </td> 
   <td colname="col4"> <p>在将文件栅格化为图像时生效。 如果以这种方式定义原始文件以覆盖徽标，则它会创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">进程</span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph">无</span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph">栅格化</span>（默认） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>仅管理资产，上传时不会创建任何衍生工具。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>按照规定的分辨率和色彩空间将文件渲染为图像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用于渲染的目标颜色空间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>在将文件栅格化为图像时生效。 如果以这种方式定义原始文件以创建覆盖徽标，则创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">进程</span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph">无</span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph">栅格化</span>（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>仅管理资产，上传时不会创建任何衍生工具。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>按照规定的分辨率和色彩空间将文件渲染为图像。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;整数&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用于渲染的目标颜色空间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布尔值&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义在呈现后是否将多页PDF合并到eCatalog中（默认为true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;布尔值&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义是否将PDF中的单词提取到数据库中以供以后提供给搜索服务器（默认值为false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您还可以从`getScheduledJobs`中查询。

已修改`webservice.gzip.response`配置属性以采用以下值之一：

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>不使用gzip响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>仅当authHeader/gzipResponse为true时，才出现Gzip响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse为true，或者不存在gzipResponse标头并且HTTP Accept-Encoding标头包含gzip，则为gzip。 （默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>始终gzip响应，不考虑标头值。 此值仅用于调试目的。 </p> </td> 
  </tr> 
 </tbody> 
</table>
