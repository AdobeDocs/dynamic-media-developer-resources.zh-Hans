---
description: 本节介绍了图像目录的功能和语法。
seo-description: 本节介绍了图像目录的功能和语法。
seo-title: 图像目录
solution: Experience Manager
title: 图像目录
topic: Scene7 Image Serving - Image Rendering API
uuid: d329807a-22b0-42a3-9297-8dad7a1dce43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像目录{#image-catalogs}

本节介绍了图像目录的功能和语法。

图像目录优惠以下功能：

* 允许将图像与某些元数据和修饰符命令永久关联。

   图像目录中的条目使用快捷记号 ` *`rootId/objId`*`，其中 ` *`rootId`*` 标识图像目录， ` *``*` objId标识目录中的数据记录。
* 为某些请求属性（如JPEG质量）提供默认值，或者是否要应用水印。
* 管理字体、ICC用户档案、宏定义和请求模板

即使未定义特定图像目录，图像目录的所有功能也可通过默认目录( [!DNL default.ini])使用。

如 ` *`果请求的URL路径中的rootId与特定图`*``attribute::RootId` 像目录的匹配，则该目录将成为此请求的主目录。 主目录提供整个请求的默认属性和设置。 如果未找到匹配项，则使用默认目录。

在或命令中标识的 `src=` 目录 `mask=` 向当前层提供以下目录属性和数据：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性／数据</b> </th> 
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
   <td> <p> 目录的 <span class="codeph"> 默认值：</span> ：如果未涉及目录记录，则当前层的到期或到期 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Icc*</span> </p> </td> 
   <td> <p> 请求和／或当前图层的工作ICC颜色用户档案、渲染方法和黑点补偿标志 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 用于当前图层的所有源文件路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Resolution</span> </p> </td> 
   <td> <p> 目录的 <span class="codeph"> 默认值：：仅分辨率</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> anchor=当 <span class="codeph"> 前图层的</span> “默认值” </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:Expiration</span> </p> </td> 
   <td> <p> 所有图层的最小过期值将用作回复图像的实时时间值 </p> </td> 
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
   <td> <p> mask=的 <span class="codeph"> 默认值</span> （当前图层） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog:::Modifier</span> </p> </td> 
   <td> <p> 当前层的前缀命令( <span class="codeph"> catalog:::Modifier</span> 中的每个命令都可以由URL中的同一命令覆盖（如果为同一层指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> 当前图层的源图像文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 当前层的后缀命令(与 <span class="codeph"> catalog:::Modifier</span>，但 <span class="codeph"> catalog::PostModifier中的命令会覆盖在URL或catalog</span> ::Modifier中指定的相 <span class="codeph"></span>同命令) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> 当前图层的对象分辨率 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一图层内， `src=` 且必 `mask=` 须引用同一图像目录（如果有）。

命令中标识的 `icc=` 目录仅用于从目录的ICC用户档案表中查找条目。 不涉及其他目录属性或数据。

如果， ` *`rootId解析为目录`*` ，并且 ` *`objId与此目录中的某个匹配，则`*` rootId/objId `catalog::Id`` *``*` 将被目录条目有效替换，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另请参阅 {#section-00e4f6b39cd14244bcce537a3f831259}

[图像目录参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
