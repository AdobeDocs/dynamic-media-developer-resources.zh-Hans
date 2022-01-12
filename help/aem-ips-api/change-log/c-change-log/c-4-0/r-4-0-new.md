---
title: 新增内容和更改
description: 介绍IPS API v4.0的新更改和已实施的更改。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 2%

---

# 新增内容和更改{#new-additions-and-changes}

介绍IPS API v4.0的新更改和已实施的更改。

通过单独的WSDL和架构命名空间并排实施了API版本。

* 以前的API版本： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

添加了 `PostScriptOptions/alpha` 字段。

添加了 `VideoRootUrl` 和 `SwfRootUrl` 属性 `getProperty` 操作。

添加了可选 `appName` 和 `appVersion` params to `authHeader` 跟踪调用应用程序。 向添加了日志记录 `ipsApiService.log`.

添加了可选 `serviceUrl` 参数到WSDL层代servlet。 此参数对于调试代理非常有用。 示例: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已实施 `getZipEntries` 操作。

实现了系统字段条件的搜索范围和键入的比较值。

添加了 `'Asset'` 资产类型字符串常量，主要用于允许跨资产元数据字段。

已实施 `trashState` 参数 `searchAssets`.

已实施 `getAssetPublishHistory` 操作。

添加了可选 `faultHttpStatusCode` 用于在Flex中启用故障处理的SOAP标头。 对于Flex，请使用 `<faultHttpStatusCode>200</faultHttpStatusCode>`. 故障响应的默认状态代码为 `500 (Internal Server Error)`.

添加了从垃圾桶恢复资产和从垃圾桶恢复空资产的操作。

已实施CRUD操作。

在 `ImageMap` 类型和 `saveImageMap` 操作。

添加了对“优化剩余文件”作业的支持。

添加了 `setAssetsPublishState` 以批量发布状态更新。

添加了 `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

已弃用 `saveMetadataField` 支持新 `createMetadataField` 和 `updateMetadataField` 操作。

已实施 `deleteAssetsParam` 批量删除操作。

已实施 `moveAssetsParam` 批量移动操作。

已实施 `deleteMetadataField` 操作。

已实施 `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` 操作。

已实施 `getAssetCounts`.

在 `setImageSetMembers` 包括 `RenderSet` 成员 `ImageSet` 资产。

添加了 `replaceImage` 操作。

添加了 `copyImage` 操作。

添加了 `setUrlModifier` 操作和 `urlModifier/urlPostApplyModifier` 字段 `LayerViewInfo`, `TemplateInfo`和 `WatermarkInfo`.

添加了 `createDerivedAsset` 操作。 当前 `ownerHandle` 必须引用图像资产，且类型可能 `AdjustedView` 或 `LayerView`.

添加了 `createTemplate` 操作。 调用以创建模板或水印资产。

IPS公司设置， `CompanySettings`，移植到Web服务API。

添加了 `excludeByproducts` 筛选标记为 `searchAssets` 操作。 将此标志设置为true会运行 `PSDlayer` 图像和PDF已撕裂的图像。

添加了 `getGenerationInfo` 操作。

添加了 `SystemMessage` 属性名称 `getProperty` 操作。

修改了一些资产类型字符串常量，以匹配相应的“资产信息”字段。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改了批处理操作的结果格式，以汇总成功、警告和错误。

已实施 `batchSetAssetMetadata` 批量元数据操作。

对特定于应用程序的数据实施了支持。

对的布尔标记实施了支持 `createTemplate`, `extendLayers`和 `extractText` 用于上传作业以控制Photoshop处理过程（与对添加文件上传的更改类似）。

已实施 `setImageMaps` 和 `setZoomTargets` 操作。

已实施 `ViewerPreset` 操作。 已识别的类型包括：

* `VideoPlayer` （视频仅发布这些查看器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

查看器外观支持两个参数： `skinFg` 和 `skinBg`. 后端代码会执行维护向后兼容性所需的所有处理。

已实施 `getAssociatedAssets` 操作。

添加了 `ReprocessAssets` 作业类型，允许重新处理以前上传的主源文件，包括重新处理PDF和重新优化图像。

已重命名 `PropertySetType` 字段类型更改为 `propertyType`. 此重命名会影响 `createPropertySetType` 参数和 `getPropertySetType/getPropertySetTypes` 响应。

已实施 `batchSetImageFields` 操作，以支持设置图像用户数据和其他可编辑的图像字段。

47向各种资产信息类型添加了fileSize字段：

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

已实施 `getActivePublishContexts` 操作。 此操作会返回一个发布上下文名称数组，其中包含指定公司的活动发布服务器。 当前发布上下文名称为：

* `ImageServing`
* `ImageRendering`
* `Video`

已实施 `getSearchStrings` 操作。 它会返回给定资产的搜索字符串数组。

添加了作业的区域设置参数以及设置API操作区域设置的机制。 区域设置字符串的格式应为 `<language_code>[-<country_code>]`. 语言代码是ISO-639指定的小写双字母代码，而可选国家/地区代码是ISO-3166指定的大写双字母代码。

在 `authHeader` 用于设置API操作的区域设置的SOAP标头。 如果此参数不存在，则HTTP标头 `Accept-Language` 中，将使用。 如果此标头不存在，则使用IPS服务器的默认区域设置。

添加了对强类型元数据字段的获取/设置支持。

实现了对gzip响应控制的SOAP和HTTP标头支持。

添加了 `gzipResponse` 标记为 `authHeader`. 如果不存在，则API会检查HTTP `Accept-Encoding` 标题。

为强类型元数据字段条件的searchAssets添加了支持。

* 对于所有字段类型，值可以使用字符串比较运算符( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* 对于布尔字段， `boolVal` 可以与 `Equals` 操作。
* 对于整型字段， `longVal` 可以使用数值比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minLong/maxLong` 可以通过数字范围运算( `Between, NotBetween`)。
* 对于浮点字段， `doubleVal` 可以使用数值比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)或 `minDouble/maxDouble` 可以通过数字范围运算( `Between, NotBetween`)。
* 对于“日期”字段，您可以 `dateVal` 与数值比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)，或者您可以传递包含数值范围运算( `Between, NotBetween`)。

添加了描述、 `jobSubType`和 `originalJobName` 字段 `JobLog` 类型。

* `originalJobName` 是提交到的作业名称 `submitJob` （没有任何唯一性后缀或后续作业名称）。
* `jobSubType` 仅用于 `ImageServingPublishJob` 工作(其中 `full`, `increment, fullwithsearch,` 或 `fulloverride`)。
* `description` 是所有作业类型的空字符串，但最终包含摘要作业信息，如上载路径。

此外，以下字段不包含在两者中 `getJobLogs` 和 `getJobLogDetails`. 在以前的版本中，它们仅可用于 `getJobLogDetails`.

* `endDate` （如果作业已完成）。
* `fileDuplicateCount` (以前， `0` with `getJobLogs`)
* `fileUpdateCount` (以前 `0` with `getJobLogs` 和 `fileSuccessCount`;现在，它被拆分为单独的字段)。

已将assetHandle字段添加到 `JobLogDetail` 类型。

向添加了可选描述参数 `submitJob`. 此参数将通过传递以在中检索 `getScheduledJobs`, `getActiveJobs`和 `getJobLogs`.

已弃用SKU系统字段。 如果字段作为 `SystemFieldCondition` to `searchAssets`.

添加了 `excludeAssetTypeArray` 筛选 `searchAssets`.

添加了 `MaskInfo` 键入 `Asset`.

添加了新的资产类型，供IPS管理：

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
   <td colname="col2"> <p>Microsoft®以.doc结尾的文件的Word文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel文档，以.xls结尾的文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint文档，用于以.ppt结尾的文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>以.rtf结尾的文件的RTF文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

添加了 `UploadDirectoryJob` 和 `UploadUrlsJob` 可单独控制Postscript、Illustrator和PDF文件的处理。 所有现有的作业都为三个处理管道中的每个管道提供了必要的参数，以便它们能够像现在一样正常工作。 原始 `PostScriptOptions` 块用于设置Illustrator和EPS/PS文件的处理。 或者，可以提供特定文件选项块以指定处理。 更改列表包括：

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 光栅化 </span>（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>仅管理资产，并且不会在上传时创建任何派生项。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以规定的分辨率和色彩空间将EPS和PostScript文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>将文件栅格化为图像时生效。 如果以这种方式定义原始文件以叠加徽标，则会创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 无 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 光栅化 </span> （默认） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>仅管理资产，并且不会在上传时创建任何派生项。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>光栅化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用于渲染的目标色彩空间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>将文件栅格化为图像时生效。 如果以这种方式定义原始文件以创建叠加徽标，则创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 光栅化 </span> （默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>仅管理资产，并且不会在上传时创建任何派生项。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>光栅化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>用于渲染的目标色彩空间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义在渲染后是否将多个页面PDF合并到eCatalog中（默认值为true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义是否将PDF中的词语提取到数据库中，以供稍后提供给搜索服务器（默认值为false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您还可以从 `getScheduledJobs`.

修改了 `webservice.gzip.response` 配置属性来获取以下值之一：

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 从未 </span> </p> </td> 
   <td colname="col2"> <p>请勿gzip响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>仅当authHeader/gzipResponse为true时，才响应Gzip。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 接受 </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse为true，或者不存在gzipResponse标头且HTTP Accept-Encoding标头包含gzip，则会设置Gzip。 (默认). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终 </span> </p> </td> 
   <td colname="col2"> <p>始终gzip响应，而不考虑标头值。 此值仅用于调试目的。 </p> </td> 
  </tr> 
 </tbody> 
</table>
