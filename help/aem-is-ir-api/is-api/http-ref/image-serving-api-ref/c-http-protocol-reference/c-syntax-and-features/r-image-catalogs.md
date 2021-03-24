---
description: 本节介绍图像目录的功能和语法。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---


# 图像目录{#image-catalogs}

本节介绍图像目录的功能和语法。

图像目录优惠以下功能：

* 允许将图像与某些元数据和修饰符命令永久关联。

   图像目录中的条目使用快捷记号`*`rootId/objId`*`进行引用，其中`*`rootId`*`标识图像目录，`*`objId`*`标识目录中的数据记录。
* 为某些请求属性（如JPEG质量或是否要应用水印）提供默认值。
* 管理字体、ICC用户档案、宏定义和请求模板

即使未定义特定图像目录，图像目录的所有功能也可通过默认目录([!DNL default.ini])使用。

如果请求的URL路径中的`*`rootId`*`与特定图像目录的`attribute::RootId`匹配，则该目录将成为此请求的主目录。 主目录提供整个请求的默认属性和设置。 如果未找到匹配项，则改用默认目录。

在`src=`或`mask=`命令中标识的目录向当前图层提供以下目录属性和数据：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性/数据</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:DefaultExt</span> </p> </td> 
   <td> <p> 当前图层中所有图像文件路径的默认扩展名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Expiration</span> </p> </td> 
   <td> <p> <span class="codeph">目录的默认值：:Expiration</span>或当前图层的到期（如果未涉及目录记录） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Icc*</span> </p> </td> 
   <td> <p> 请求和/或当前图层的工作ICC颜色用户档案、渲染方法和黑点补偿标志 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 用于当前图层的所有源文件路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Resolution</span> </p> </td> 
   <td> <p> <span class="codeph">目录的默认值：:Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：锚点</span> </p> </td> 
   <td> <p> 当前图层的<span class="codeph"> anchor=</span>值的默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:Expiration</span> </p> </td> 
   <td> <p> 所有图层的最小过期值用作回复图像的生存时间值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 当前图层的源图像颜色用户档案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> 当前图层的图像映射数据 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 当前图层的<span class="codeph"> mask=</span>默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> 当前图层的前缀命令(<span class="codeph">目录：:Modifier</span>中的每个命令都可以由URL中的同一命令覆盖（如果为同一图层指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 当前图层的源图像文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 当前图层的后缀命令（与<span class="codeph">目录：:Modifier</span>类似，但<span class="codeph">目录：:PostModifier</span>中的命令会覆盖在URL或<span class="codeph">目录：:Modifier</span>中指定的相同命令） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 当前图层的对象分辨率 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一图层内，`src=`和`mask=`必须引用同一图像目录（如果有）。

`icc=`命令中标识的目录仅用于从目录的ICC用户档案表查找条目。 不涉及其他目录属性或数据。

如果`*`rootId`*`解析为目录，且`*`objId`*`与此目录中的`catalog::Id`匹配，则`*`rootId/objId`*`将被目录条目有效替换，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另请参阅 {#section-00e4f6b39cd14244bcce537a3f831259}

[图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)=, [遮罩=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
