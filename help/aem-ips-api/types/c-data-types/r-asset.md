---
description: 文件夹层次结构中的对象或容器。
seo-description: 文件夹层次结构中的对象或容器。
seo-title: 资源
solution: Experience Manager
title: 资源
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 动 <span class="varname"> 画GifInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AnimatedGifInfo</span> </td> 
   <td colname="col3"> 有关动画GIF文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 资 <span class="varname"> 产句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 资产句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> cabinet <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:CabinetInfo</span> </td> 
   <td colname="col3"> 文件柜资源类型的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 已 <span class="varname"> 创建</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上传资产的日期和时间。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 创建资产的用户的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> css信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：CssInfo</span> </td> 
   <td colname="col3"> 有关CSS文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excel信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">返回虚拟文件名。 完整的虚拟文件路径是 <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flash信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文 <span class="varname"> 件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 包含资产的文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文件 <span class="varname"> 夹处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 处理资产的父文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> 字体资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> iccProfileInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:IccProfileInfo</span> </td> 
   <td colname="col3"> ICC用户档案资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustrator信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ImageInfo</span> </td> 
   <td colname="col3"> 图像资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 相对URL，表示资产的缩略图视图。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> javascript <span class="varname"> 信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：JavascriptInfo</span> </td> 
   <td colname="col3"> 有关JavaScript文件的详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上次 <span class="varname"> 修改时间</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次修改资产的日期和时间。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上次修改资产的用户的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:LayerViewInfo</span> </td> 
   <td colname="col3"> 图层视图资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 遮 <span class="varname"> 罩信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 元 <span class="varname"> 数据数组</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：MetadataArray</span> </td> 
   <td colname="col3"> 与资产关联的元数据值的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 资产名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf设置信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF设置资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 权 <span class="varname"> 限</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 项 <span class="varname"> 目</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 列表项目名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psd信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 就 <span class="varname"> 绪发布</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 设置一个标志以指示是否应发布资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:RenderSceneInfo</span> </td> 
   <td colname="col3"> 渲染场景资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> rtf <span class="varname"> 信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 子 <span class="varname"> 类型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">支持子类型值的常规资产子类型(例如 <span class="codeph"> Asset</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> svg <span class="varname"> 信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：SvgInfo</span> </td> 
   <td colname="col3"> SVG资源的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：SwcInfo</span> </td> 
   <td colname="col3"> SWC资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 模 <span class="varname"> 板信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TemplateInfo</span> </td> 
   <td colname="col3"> 模板资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 垃圾 <span class="varname"> 状态</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指示资产是位于垃圾桶中还是处于实时状态（有关值，请参阅“垃圾桶状态”）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 类型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">资源类型. 有关值 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 的信息</a> ，请参阅资产类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> videoCaptionInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>视频题注资产的属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> video <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> <p>视频资产的属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> viewerPresetInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ViewerPresetInfo</span> </td> 
   <td colname="col3"> 查看器预设资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ViewerSwfInfo</span> </td> 
   <td colname="col3"> 查看器SWf资源的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 暗角信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：暗角信息</span> </td> 
   <td colname="col3"> 暗角资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 水 <span class="varname"> 印信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:WatermarkInfo</span> </td> 
   <td colname="col3"> 水印资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 窗 <span class="varname"> 口CoveringInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:WindowCoveringInfo</span> </td> 
   <td colname="col3"> 覆盖资产的窗口的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xml信息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：XmlInfo</span> </td> 
   <td colname="col3"> XML资产的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：XslInfo</span> </td> 
   <td colname="col3"> XSL资源的属性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

