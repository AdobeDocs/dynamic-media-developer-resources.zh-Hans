---
description: 介绍IPS API v4.0的新更改和实现的更改。
seo-description: 介绍IPS API v4.0的新更改和实现的更改。
seo-title: 新增和更改
solution: Experience Manager
title: 新增和更改
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 2%

---


# 新增和更改{#new-additions-and-changes}

介绍IPS API v4.0的新更改和实现的更改。

并排实施了API版本，并分别使用了不同的WSDL和模式命名空间。

* 以前的API版本：`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`。
* SPS 4.0版本：`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`。

添加了`PostScriptOptions/alpha`字段。

为`getProperty`操作添加了`VideoRootUrl`和`SwfRootUrl`属性。

为`authHeader`添加了可选的`appName`和`appVersion`参数以跟踪调用的应用程序。 已向`ipsApiService.log`添加日志记录。

为WSDL生成servlet添加了可选`serviceUrl`参数。 这对于调试代理特别有用。 示例: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

已实现`getZipEntries`操作。

实现了系统字段条件的搜索范围和类型比较值。

添加了`'Asset'`资产类型字符串常量，主要用于允许跨资产元数据字段。

为`searchAssets`实现了`trashState`参数。

已实现`getAssetPublishHistory`操作。

添加了可选的`faultHttpStatusCode` SOAP头，以在Flex中启用错误处理。 对于Flex，请使用`<faultHttpStatusCode>200</faultHttpStatusCode>`。 故障响应的默认状态代码为`500 (Internal Server Error)`。

添加了从废纸篓恢复资源和从废纸篓清空资源的操作。

已实施CRUD操作。

为`ImageMap`类型和`saveImageMap`操作添加了启用标志。

增加了对“优化剩余文件”作业的支持。

为批量发布状态更新添加了`setAssetsPublishState`。

添加了`ImageServingPublishSettings`、`getImageServingPublishSettings`、`setImageServingPublishSettings`。

已弃用`saveMetadataField`操作，而使用新的`createMetadataField`和`updateMetadataField`操作。

实施了`deleteAssetsParam`批删除操作。

已实施`moveAssetsParam`批移动操作。

已实现`deleteMetadataField`操作。

已实施`get/setImageRenderingPublishSettings`、`get/set/create/updateVignettePublishFormat`操作。

已实现`getAssetCounts`。

增加了对`setImageSetMembers`的支持，以在`ImageSet`资产中包含`RenderSet`成员。

添加了`replaceImage`操作。

添加了`copyImage`操作。

为`LayerViewInfo`、`TemplateInfo`和`WatermarkInfo`添加了`setUrlModifier`操作和`urlModifier/urlPostApplyModifier`字段。

添加了`createDerivedAsset`操作。 当前，`ownerHandle`必须引用图像资产，类型可以是`AdjustedView`或`LayerView`。

添加了`createTemplate`操作。 当前，可以调用此值来创建模板或水印资产。

IPS公司设置`CompanySettings`可移植到Web服务API。

已将`excludeByproducts`过滤器标志添加到`searchAssets`操作。 将此标志设置为true将运行`PSDlayer`图像和PDF翻录图像。

添加了`getGenerationInfo`操作。

已将`SystemMessage`属性名称添加到`getProperty`操作。

修改了某些资产类型字符串常量以匹配相应的“资产信息”字段。

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

修改了批处理操作的结果格式，以汇总成功、警告和错误。

已实施`batchSetAssetMetadata`批元数据操作。

实现了对应用程序特定数据的支持。

实现了对`createTemplate`、`extendLayers`和`extractText`的布尔标志的支持，以上传作业以控制Photoshop处理过程（与添加文件上载的更改类似）。

已实施`setImageMaps`和`setZoomTargets`操作。

已实施`ViewerPreset`操作。 可识别的类型有：

* `VideoPlayer` （视频仅发布这些查看器。）
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

查看器外观支持两个参数：`skinFg`和`skinBg`。 后端代码将执行保持向后兼容性所需的所有处理。

已实现`getAssociatedAssets`操作。

添加了`ReprocessAssets`作业类型以允许重新处理以前上传的主源文件，包括重新翻录PDF和重新优化图像。

已将`PropertySetType`字段类型重命名为`propertyType`。 这会影响`createPropertySetType`参数和`getPropertySetType/getPropertySetTypes`响应。

实现了`batchSetImageFields`操作，以支持设置图像用户数据和其他可编辑的图像字段。

47将fileSize字段添加到各种资产信息类型：

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

已实现`getActivePublishContexts`操作。 此操作返回具有指定公司的活动发布服务器的发布上下文名称数组。 当前发布上下文名称为：

* `ImageServing`
* `ImageRendering`
* `Video`

已实现`getSearchStrings`操作。 它返回给定资产的搜索字符串数组。

添加了作业的区域设置参数和设置API操作区域设置的机制。 区域设置字符串的格式应为`<language_code>[-<country_code>]`。 语言代码是ISO-639指定的小写、双字母代码，可选国家/地区代码是ISO-3166指定的大写、双字母代码。

向`authHeader` SOAP头中添加了可选区域设置参数，以设置API操作的区域设置。 如果此参数不存在，将使用HTTP头`Accept-Language`。 如果此头也不存在，则将使用IPS服务器的默认区域设置。

添加了对强类型元数据字段的获取/设置支持。

实现了对gzip响应控制的SOAP和HTTP头支持。

已将`gzipResponse`标志添加到`authHeader`。 如果不存在，API还将检查HTTP `Accept-Encoding`头。

为强类型化元数据字段条件的searchAssets添加了支持。

* 对于所有字段类型，值可以用字符串比较运算符(`Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)传递
* 对于布尔字段，`boolVal`可以与`Equals` op一起传递。
* 对于Int字段，`longVal`可以用数字比较运算符(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)传递，或`minLong/maxLong`可以用数字范围运算(`Between, NotBetween`)传递。
* 对于“浮点”字段，`doubleVal`可以用数字比较运算符(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)传递，或`minDouble/maxDouble`可以用数字范围运算(`Between, NotBetween`)传递。
* 对于“日期”字段，您可以传递带数字比较运算符(`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)的`dateVal`，也可以传递带数字范围运算(`Between, NotBetween`)的minDate/maxDate。

将描述、`jobSubType`和`originalJobName`字段添加到`JobLog`类型。

* `originalJobName` 是提交到的作 `submitJob` 业名称（没有任何唯一性后缀或后续作业名称）。
* `jobSubType` 当前仅供作 `ImageServingPublishJob` 业使用(其中属于 `full`或 `increment, fullwithsearch,` 之一 `fulloverride`)。
* `description` 当前是所有作业类型的空字符串，但最终将包含摘要作业信息，如上载路径。

此外，`getJobLogs`和`getJobLogDetails`中不包含以下字段。 在旧版本中，它们只能用于`getJobLogDetails`。

* `endDate` （如果作业已完成）。
* `fileDuplicateCount` (以前一直 `0` 在 `getJobLogs`)
* `fileUpdateCount` (以前总是 `0` 与 `getJobLogs` 一起并包含 `fileSuccessCount`;现在，它被拆分为单独的字段)。

已将assetHandle字段添加到`JobLogDetail`类型。

向`submitJob`添加了可选描述参数。 传递此信息以在`getScheduledJobs`、`getActiveJobs`和`getJobLogs`中进行检索。

已弃用SKU系统字段。 如果字段作为`SystemFieldCondition`传入`searchAssets`，则忽略该字段。

已将`excludeAssetTypeArray`筛选器添加到`searchAssets`。

已将`MaskInfo`类型添加到`Asset`。

添加了新的资源类型，供IPS管理：

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>针对以.doc结尾的文件的Microsoft Word文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>针对以.xls结尾的文件的Microsoft Excel文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>针对以.ppt结尾的文件的Microsoft PowerPoint文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>适用于以.rtf结尾的文件的RTF文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

为`UploadDirectoryJob`和`UploadUrlsJob`添加了其他选项，以独立控制Postscript、Illustrator和PDF文件的处理。 所有现有作业都将为3条处理管道中的每条提供必要的参数，以使它们能够像现在一样正常工作。 原始`PostScriptOptions`块用于设置Illustrator和EPS/PS文件的处理。 或者，可以提供特定文件选项块以指定处理。 更改的列表包括：

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 栅格 </span>化（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>仅管理资产，不要在上传时创建任何衍生项。 </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>以规定的分辨率和色彩空间将EPS和PostScript文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>将文件栅格化为图像时生效。 如果以这种方式定义原始文件以覆盖徽标，它将创建透明的背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> Illustrator选项  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 无 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 栅格 </span> 化（默认） </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>仅管理资产，不要在上传时创建任何衍生项。 </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 分辨率  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>目标色彩空间进行渲染。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>可选。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>将文件栅格化为图像时生效。 如果以这种方式定义原始文件以创建叠加徽标，则创建透明背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 进度 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 无 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 栅格 </span> 化（默认） </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>仅管理资产，不要在上传时创建任何衍生项。 </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>以规定的分辨率和色彩空间将文件渲染到图像中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 分辨率  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>栅格化分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 颜色空间 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>目标色彩空间进行渲染。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义渲染后是否将多页PDF合并到电子目录中（默认为true）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>定义是否将PDF中的单词提取到数据库中，以供以后提供给搜索服务器（默认为false）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您还可以从`getScheduledJobs`进行查询。

已修改`webservice.gzip.response`配置属性，以采用以下值之一：

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
   <td colname="col2"> <p>不要压缩响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>仅当authHeader/gzipResponse为true时，Gzip响应。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 接受 </span> </p> </td> 
   <td colname="col2"> <p>如果authHeader/gzipResponse为true，或者不存在gzipResponse头且HTTP接受编码头包含gzip，则Gzip为Gzip。 (默认). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终 </span> </p> </td> 
   <td colname="col2"> <p>始终gzip响应，而不考虑标头值。 此值仅用于调试目的。 </p> </td> 
  </tr> 
 </tbody> 
</table>

