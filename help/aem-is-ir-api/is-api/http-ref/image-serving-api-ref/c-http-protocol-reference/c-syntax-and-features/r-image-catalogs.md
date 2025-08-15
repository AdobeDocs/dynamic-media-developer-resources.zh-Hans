---
description: 本节介绍了图像目录的特性和语法。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# 图像目录{#image-catalogs}

本节介绍了图像目录的特性和语法。

图像目录提供以下功能：

* 允许将图像与某些元数据和修饰符命令永久关联。

  图像目录中的条目使用快捷方式`*`rootId/objId`*`引用，其中`*`rootId`*`标识图像目录，`*`objId`*`标识目录中的数据记录。
* 为某些请求属性提供默认值，例如JPEG质量或是否要应用水印。
* 管理字体、ICC配置文件、宏定义和请求模板

即使未定义特定的图像目录，图像目录的所有功能也可通过默认目录([!DNL default.ini])使用。

如果请求的URL路径中的`*`rootId`*`与特定图像目录的`attribute::RootId`匹配，则该目录将成为此请求的主目录。 主目录提供整个请求的默认属性和设置。 如果未找到匹配项，则改用默认目录。

在`src=`或`mask=`命令中标识的目录为当前层提供以下目录属性和数据：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>属性/数据</b> </th> 
   <th class="entry"> <b>备注</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">属性：：DefaultExt</span> </p> </td> 
   <td> <p> 当前图层中所有图像文件路径的默认扩展名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：Expiration</span> </p> </td> 
   <td> <p> <span class="codeph">目录的默认值：：Expiration</span>，如果不涉及目录记录，则为当前层过期 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：Icc*</span> </p> </td> 
   <td> <p> 请求和/或当前图层的工作ICC颜色配置文件、渲染意图和黑色点补偿标记 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：RootPath</span> </p> </td> 
   <td> <p> 用于当前层的所有源文件路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：Resolution</span> </p> </td> 
   <td> <p> <span class="codeph">目录的默认值：：仅分辨率</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：锚点</span> </p> </td> 
   <td> <p> 当前图层的<span class="codeph">锚点=</span>值的默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：过期</span> </p> </td> 
   <td> <p> 所有图层的最小过期值都用作回复图像的生存时间值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：IccProfile</span> </p> </td> 
   <td> <p> 当前图层的源图像颜色配置文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：Map</span> </p> </td> 
   <td> <p> 当前图层的图像映射数据 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：MaskPath</span> </p> </td> 
   <td> <p> 当前图层的<span class="codeph">掩码的默认值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：Modifier</span> </p> </td> 
   <td> <p> 当前层的前缀命令（如果为同一层指定，<span class="codeph"> catalog：：Modifier</span>中的每个命令都可以由URL中的相同命令覆盖） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：路径</span> </p> </td> 
   <td> <p> 当前图层的源图像文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：PostModifier</span> </p> </td> 
   <td> <p> 当前层的后缀命令（类似于<span class="codeph"> catalog：：Modifier</span>，但<span class="codeph"> catalog：：PostModifier</span>中的命令覆盖在URL或<span class="codeph"> catalog：：Modifier</span>中指定的相同命令） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：Resolution</span> </p> </td> 
   <td> <p> 当前图层的对象分辨率 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一图层中，`src=`和`mask=`必须引用相同的图像目录（如果有）。

`icc=`命令中标识的目录仅用于从该目录的ICC配置文件表中查找条目。 不涉及其他目录属性或数据。

如果`*`rootId`*`解析为目录，且`*`objId`*`与此目录中的`catalog::Id`匹配，则`*`rootId/objId`*`将被目录条目有效地替换，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另请参阅 {#section-00e4f6b39cd14244bcce537a3f831259}

[图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)，[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)，[蒙版=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，[锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
