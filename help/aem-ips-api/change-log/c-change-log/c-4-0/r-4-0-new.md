---
description: 介绍IPS API v4.0的新更改和实现的更改。
seo-description: 介绍IPS API v4.0的新更改和实现的更改。
seo-title: 新增功能和更改
solution: Experience Manager
title: 新增功能和更改
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 新增功能和更改{#new-additions-and-changes}

介绍IPS API v4.0的新更改和实现的更改。

使用单独的WSDL和模式命名空间并排实施API版本。

* 先前的API版本： `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0版本： `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

已添加 `PostScriptOptions/alpha` 字段。

添加 `VideoRootUrl` 了操 `SwfRootUrl` 作的属性 `getProperty` 和属性。

添加了可 `appName` 选和 `appVersion` 参数以跟 `authHeader` 踪调用应用程序。 已向添加日志记 `ipsApiService.log`录。

为WSDL代servlet添 `serviceUrl` 加了一个可选参数。 这对于调试代理特别有用。 示例: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已实施 `getZipEntries` 操作。

实现了系统字段条件的搜索范围和类型比较值。

添加 `'Asset'` 了资产类型字符串常数，主要用于允许跨资产元数据字段。

已实 `trashState` 现的参数 `searchAssets`。

已实施 `getAssetPublishHistory` 操作。

添加了可 `faultHttpStatusCode` 选的SOAP头，以在Flex中启用故障处理。 对于Flex，请使用 `<faultHttpStatusCode>200</faultHttpStatusCode>`。 故障响应的默认状态代码为 `500 (Internal Server Error)`。

添加了从垃圾桶中恢复资源和从垃圾桶中清空资源的操作。

实施了CRUD操作。

为类型和操作添 `ImageMap` 加了启用 `saveImageMap` 标志。

增加了对“优化剩余文件”作业的支持。

为批量 `setAssetsPublishState` 发布状态更新添加了内容。

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

已弃 `saveMetadataField` 用的操作，而不是新的 `createMetadataField` 和 `updateMetadataField` 操作。

实施 `deleteAssetsParam` 了批删除操作。

已实 `moveAssetsParam` 施批量移动操作。

已实施 `deleteMetadataField` 操作。

已实 `get/setImageRenderingPublishSettings`施， `get/set/create/updateVignettePublishFormat` 操作。

Implemented `getAssetCounts`.

增加了对在资 `setImageSetMembers` 产中包含 `RenderSet` 成员的 `ImageSet` 支持。

添加了 `replaceImage` 操作。

添加了 `copyImage` 操作。

为、 `setUrlModifier` 和添加 `urlModifier/urlPostApplyModifier` 了操 `LayerViewInfo`作和 `TemplateInfo`字段 `WatermarkInfo`。

添加了 `createDerivedAsset` 操作。 当前必 `ownerHandle` 须引用图像资产，且类型可能为 `AdjustedView` 或 `LayerView`。

添加了 `createTemplate` 操作。 当前，可以调用此选项来创建模板或水印资产。

IPS公司设置， `CompanySettings`移植到Web服务API。

为操作 `excludeByproducts` 添加了过滤器 `searchAssets` 标志。 将此标志设置为true可运行图 `PSDlayer` 像和PDF翻录的图像。

添加了 `getGenerationInfo` 操作。

为操作 `SystemMessage` 添加了属性 `getProperty` 名称。

修改了一些资产类型字符串常量以匹配相应的资产信息字段。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改了批处理操作的结果格式，以汇总成功、警告和错误。

实施了 `batchSetAssetMetadata` 批量元数据操作。

实施了对特定于应用程序的数据的支持。

实现了对布尔标记的支 `createTemplate`持， `extendLayers`以及上 `extractText` 传作业以控制Photoshop处理过程（与添加文件上传的更改类似）。

实施 `setImageMaps` 和 `setZoomTargets` 操作。

已实施 `ViewerPreset` 操作。 可识别的类型有：

* `VideoPlayer` （视频仅发布这些查看器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

查看器外观支持两个参数： `skinFg` 和 `skinBg`。 后端代码将执行保持向后兼容性所需的所有处理。

已实施 `getAssociatedAssets` 操作。

添加 `ReprocessAssets` 了作业类型，以允许重新处理以前上传的主文件，包括重新翻录PDF和重新优化图像。

将字 `PropertySetType` 段类型重命名为 `propertyType`。 这会影响参 `createPropertySetType` 数和响 `getPropertySetType/getPropertySetTypes` 应。

实现了 `batchSetImageFields` 支持设置图像用户数据和其他可编辑图像字段的操作。

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

已实施 `getActivePublishContexts` 操作。 此操作将返回一组具有指定公司的活动发布服务器的发布上下文名称。 当前发布上下文名称为：

* `ImageServing`
* `ImageRendering`
* `Video`

已实施 `getSearchStrings` 操作。 它返回给定资产的搜索字符串数组。

为作业添加了区域设置参数，并添加了一种为API操作设置区域设置的机制。 区域设置字符串的格式应设置为 `<language_code>[-<country_code>]`。 语言代码是ISO-639指定的小写双字母代码，可选国家／地区代码是ISO-3166指定的大写双字母代码。

向SOAP头中添加了可选的 `authHeader` 区域设置参数，以设置API操作的区域设置。 如果此参数不存在，则将使 `Accept-Language` 用HTTP头。 如果此头也不存在，则将使用IPS服务器的默认区域设置。

增加了对强类型元数据字段的获取／设置支持。

实现了对gzip响应控制的SOAP和HTTP头支持。

向中 `gzipResponse` 添加了标 `authHeader`志。 如果它不存在，API还将检查HTTP头 `Accept-Encoding` 。

为searchAssets添加了对强类型元数据字段条件的支持。

* 对于所有字段类型，值可以与字符串比较运算符( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)一起传递
* 对于布尔字段， `boolVal` 可以与op一起传 `Equals` 递。
* 对于Int字段， `longVal` 可以使用数字比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)传递，也 `minLong/maxLong` 可以使用数字范围运算( `Between, NotBetween`)传递。
* 对于“浮动”字 `doubleVal` 段，可以使用数字比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)传递， `minDouble/maxDouble` 也可以使用数字范围运算( `Between, NotBetween`)传递。
* 对于“日期”字段，您可以 `dateVal` 使用数字比较运算符( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)传递，或者可以使用数字范围运算传递minDate/maxDate( `Between, NotBetween`)。

为类型添 `jobSubType`加了说明 `originalJobName` 、和字 `JobLog` 段。

* `originalJobName` 是提交到的作业名 `submitJob` 称（没有任何唯一性后缀或后续作业名称）。
* `jobSubType` 当前仅供作 `ImageServingPublishJob` 业使用(其中属于或 `full``increment, fullwithsearch,` 之一 `fulloverride`)。
* `description` 当前为所有作业类型的空字符串，但最终将包含摘要作业信息，如上传路径。

此外，以下字段不包含在和中 `getJobLogs` 间 `getJobLogDetails`。 在以前版本中，它们只提供 `getJobLogDetails`。

* `endDate` （如果作业已完成）。
* `fileDuplicateCount` (以前一直 `0` 在 `getJobLogs`)
* `fileUpdateCount` (以前一直与 `0` 其一 `getJobLogs` 起并纳入其中 `fileSuccessCount`;现在，它被拆分为单独的字段)。

添加了要键入的assetHandle `JobLogDetail` 字段。

向添加了可选的描述参数 `submitJob`。 这是传递的，用于在、 `getScheduledJobs`和 `getActiveJobs`中检索 `getJobLogs`。

已弃用SKU系统字段。 如果字段作为传入对象传入，则忽略该 `SystemFieldCondition` 字段 `searchAssets`。

已向 `excludeAssetTypeArray` 添加过滤 `searchAssets`器。

已将类 `MaskInfo` 型添加到 `Asset`。

添加了新的资源类型，以供IPS管理：

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
   <td colname="col2"> <p>针对以。doc结尾的文件的Microsoft Word文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>针对以。xls结尾的文件的Microsoft Excel文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>针对以。ppt结尾的文件的Microsoft PowerPoint文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>用于以。rtf结尾上传的文件的RTF文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

为Postscript、Illustrator和PDF文 `UploadDirectoryJob` 件单独 `UploadUrlsJob` 添加了其他选项，并可单独控制处理这些文件。 所有现有作业都将为3条处理管道中的每一条提供必要的参数，使它们能够像现在一样正常工作。 原始 `PostScriptOptions` 块用于设置Illustrator和EPS/PS文件的处理。 或者，可以提供特定文件选项块以指定处理。 更改的列表包括：

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
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 栅格 </span>化（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>仅管理资产，不要在上传时创建任何衍生产品。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以规定的分辨率和色彩空间将EPS和PostScript文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>将文件栅格化为图像时生效。 如果以这种方式定义原始文件以覆盖徽标，它将创建透明的背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> Illustrator选项 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 无 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 栅格 </span> 化（默认） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>仅管理资产，不要在上传时创建任何衍生产品。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 分辨率 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>目标色彩空间进行渲染。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>在将文件栅格化为图像时生效。 如果以这种方式定义原始文件以创建叠加徽标，则创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 栅格 </span> 化（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>仅管理资产，不要在上传时创建任何衍生产品。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 分辨率 </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>目标色彩空间进行渲染。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义渲染后是否将多页PDF合并到eCatalog中（默认为true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义是否将PDF中的单词提取到DB中以供以后提供给搜索服务器（默认为false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您还可以从中查询 `getScheduledJobs`。

修改了 `webservice.gzip.response` 配置属性以采用以下值之一：

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
   <td colname="col2"> <p>仅当authHeader/gzipResponse为true时，Gzip响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 接受 </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse为true，或者不存在gzipResponse头且HTTP Accept-Encoding头包含gzip，则为Gzip。 (默认). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终 </span> </p> </td> 
   <td colname="col2"> <p>始终gzip响应，而不考虑标题值。 此值仅用于调试目的。 </p> </td> 
  </tr> 
 </tbody> 
</table>

