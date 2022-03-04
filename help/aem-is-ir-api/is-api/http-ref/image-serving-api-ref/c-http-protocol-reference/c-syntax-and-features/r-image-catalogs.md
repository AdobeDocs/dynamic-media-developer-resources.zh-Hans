---
description: 此部分介绍了图像目录的功能和语法。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# 图像目录{#image-catalogs}

此部分介绍了图像目录的功能和语法。

图像目录提供以下功能：

* 允许将图像与某些元数据和修饰符命令永久关联。

   图像目录中的条目使用快捷键表示法进行引用 `*`rootId/objId`*`，其中 `*`rootId`*` 识别图像目录和 `*`objId`*` 在目录中标识数据记录。
* 为某些请求属性(如JPEG质量或是否要应用水印)提供默认值。
* 管理字体、ICC配置文件、宏定义和请求模板

即使未定义任何特定的图像目录，图像目录的所有功能也可通过默认目录( [!DNL default.ini])。

如果 `*`rootId`*` 在请求的URL路径中匹配 `attribute::RootId` ，则该目录将成为此请求的主目录。 主目录提供了整个请求的默认属性和设置。 如果未找到匹配项，则改用默认目录。

在 `src=` 或 `mask=` 命令向当前层提供以下目录属性和数据：

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
   <td> <p> 当前层中所有图像文件路径的默认扩展名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Expiration</span> </p> </td> 
   <td> <p> 默认 <span class="codeph"> 目录：：过期</span> 或当前层的到期（如果未涉及目录记录） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Icc*</span> </p> </td> 
   <td> <p> 请求和/或当前层的工作ICC颜色配置文件、渲染意图和黑点补偿标记 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:RootPath</span> </p> </td> 
   <td> <p> 用于当前层的所有源文件路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Resolution</span> </p> </td> 
   <td> <p> 默认 <span class="codeph"> 目录：:Resolution</span> 仅 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：锚点</span> </p> </td> 
   <td> <p> 默认 <span class="codeph"> 锚点=</span> 当前层的值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：过期</span> </p> </td> 
   <td> <p> 所有层的最小过期值都用作回复图像的生存时间值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> 当前图层的源图像颜色配置文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:Map</span> </p> </td> 
   <td> <p> 当前层的图像映射数据 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> 默认 <span class="codeph"> 掩码=</span> 对于当前层 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：修饰符</span> </p> </td> 
   <td> <p> 当前层的前缀命令( <span class="codeph"> 目录：：修饰符</span> 可以由URL中的相同命令覆盖（如果为同一层指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：路径</span> </p> </td> 
   <td> <p> 当前图层的源图像文件 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> 当前层的后缀命令(类似于 <span class="codeph"> 目录：：修饰符</span>，但是 <span class="codeph"> catalog::PostModifier</span> 覆盖URL或 <span class="codeph"> 目录：：修饰符</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:Resolution</span> </p> </td> 
   <td> <p> 当前层的对象分辨率 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一层， `src=` 和 `mask=` 必须引用相同的图像目录（如果有）。

在 `icc=` 命令仅用于从目录的ICC配置文件表查找条目。 不涉及其他目录属性或数据。

如果， `*`rootId`*` 解析为目录，和 `*`objId`*` 与 `catalog::Id` 然后， `*`rootId/objId`*` 实际上已被目录条目所替换，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另请参阅 {#section-00e4f6b39cd14244bcce537a3f831259}

[图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [掩码=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
