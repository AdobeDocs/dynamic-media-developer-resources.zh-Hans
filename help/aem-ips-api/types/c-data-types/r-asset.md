---
description: 文件夹层次结构中的对象或容器。
solution: Experience Manager
title: 资源
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 7%

---

# 资源{#asset}

文件夹层次结构中的对象或容器。

语法

## 参数 {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> animatedGifInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AnimatedGifInfo</span> </td> 
   <td colname="col3"> 有关GIF动画文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 资产句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cabinetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：CabinetInfo</span> </td> 
   <td colname="col3"> 文件柜资产类型的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 已创建</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上传资产的日期和时间。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 创建资产的用户的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：CssInfo</span> </td> 
   <td colname="col3"> 有关CSS文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">返回虚拟文件名。 完整的虚拟文件路径为<span class="codeph">文件夹</span>+<span class="codeph"> fileName</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 文件夹</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 包含资产的文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 处理资产的父文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> 字体资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> iccProfileInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:IccProfileInfo</span> </td> 
   <td colname="col3"> ICC配置文件资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ImageInfo</span> </td> 
   <td colname="col3"> 图像资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 相对URL，表示资产的缩略图视图。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：JavascriptInfo</span> </td> 
   <td colname="col3"> 有关JavaScript文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModified</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次修改资产的日期和时间。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上次修改资产的用户的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:LayerViewInfo</span> </td> 
   <td colname="col3"> 层视图资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MetadataArray</span> </td> 
   <td colname="col3"> 与资产关联的元数据值数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 资产名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF设置资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 权限</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 项目</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 项目名称列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 设置一个标志以指示是否应发布资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:RenderSceneInfo</span> </td> 
   <td colname="col3"> 呈现场景资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">支持子类型值的通用资产子类型（例如，<span class="codeph"> AssetSet</span>）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：SvgInfo</span> </td> 
   <td colname="col3"> SVG资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：SwcInfo</span> </td> 
   <td colname="col3"> SWC资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TemplateInfo</span> </td> 
   <td colname="col3"> 模板资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指示资产是处于垃圾桶中还是处于实时状态（有关值，请参阅“垃圾桶状态”）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">资源类型. 有关值，请参阅<a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local">资产类型</a> 。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>视频标题资产的属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> <p>视频资产的属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ViewerPresetInfo</span> </td> 
   <td colname="col3"> 查看器预设资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ViewerSwfInfo</span> </td> 
   <td colname="col3"> 查看器SWf资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VignetteInfo</span> </td> 
   <td colname="col3"> 晕影资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：WatermarkInfo</span> </td> 
   <td colname="col3"> 水印资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:WindowCoveringInfo</span> </td> 
   <td colname="col3"> 覆盖资产的窗口的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:XmlInfo</span> </td> 
   <td colname="col3"> XML资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：XslInfo</span> </td> 
   <td colname="col3"> XSL资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
