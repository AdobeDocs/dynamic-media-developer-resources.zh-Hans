---
title: src
description: 材料文件。 以单个材质目录引用的形式指定材质数据，或者以逗号分隔的一个或两个图像或材质数据文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---

# src{#src}

材料文件。 以单个材质目录引用的形式指定材质数据，或者以逗号分隔的一个或两个图像或材质数据文件。

`src = *`catalogEntry`*|{{ *`材料文件`*| *`embeddedReq`*}[, *`材料文件`*]`

`srcE= *`名称`*`

`srcN= *`指数`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> 材料文件</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 样式文件</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">大括号；'是&amp;lbrace；'<span class="varname"> isReq</span>'&amp;rbrace；'&amp;rbrace；|&amp;lbrace；'ir&amp;lbrace；'<span class="varname"> irReq</span>'&amp;rbrace；'|&amp;lbrace；'&amp;lbrace；'<span class="varname"> foreignReq</span>'&amp;rbrace；'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>材质目录ID (<span class="codeph"> attribute：：RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>物料目录条目(<span class="codeph"> catalog：：Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 样式文件</span> </p></td> 
  <td class="stentry"> <p>材料样式文件(<span class="filepath"> .vnc</span> 或 <span class="filepath"> .vnw</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>图像数据文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>请求图像服务。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>图像渲染请求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>请求到外部服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名称</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的名称。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 指数</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的从0开始的索引号。 </p></td> 
 </tr> 
</table>

可重复的纹理、贴花和壁纸材料需要单个图像，它可以指定为文件或嵌入请求。

机柜材料需要机柜样式的文件( [!DNL .vnc])，不能指定为嵌套请求。 对于文件柜而言，纹理图像文件是可选的，如果指定，它可以是一个文件，也可以是嵌入的请求。

窗饰材料需要窗饰样式文件( [!DNL .vnw])，不能指定为嵌套请求。 纹理文件是可选的，如果指定，它可以是一个文件，也可以是嵌入的请求。

图像渲染使用与图像服务相同的规则来查找材质目录、目录条目和数据文件。 请参阅 *`object`* 详细信息，请参阅图像服务文档中的数据类型。

*`materialFile`* 是相对于 `attribute::RootPath`.

*`foreignReq`* 可以是URL的相对于 `attribute::RootUrl`，或者绝对URL，如果 `attribute::AllowDirectUrls` 设置。

如果 *`catId`* 未指定，将使用会话目录。

`srcE=` 和 `srcN=` 提供对晕影中嵌入的材料的访问。

## 支持的文件格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

图像渲染支持与Dynamic Media图像服务相同的源图像格式。

当使用Scene7金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 图像服务包括从任何支持的格式创建PTIFF图像的图像转换器(IC)实用程序。

有关支持的文件格式的完整列表，请参阅“图像服务”文档中的IC实用程序说明。

## 属性 {#section-e68d03788d534e2184147987d51dfd0f}

材质属性。 对于除纯色以外的所有材料都需要（纯色材料不允许使用）。 所有字符串都区分大小写。 *`index`* 必须为0或更大。

## 默认 {#section-dde549c1917540dc8f9555962202da3c}

无。

## 示例 {#section-675865444f8a4d35b9fc6e58b36e3438}

具有单独可重复纹理的彩色机柜的MSS：

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

材质目录中可以包含相同的材质 `'cat`&#39;在记录中&#39; `12-3-2`&#39;：

`…&obj=cabinets&src=cat/12-3-2&…`

对图像服务的嵌套请求以获取纹理图像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另请参阅 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[物料目录](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)， [attribute：：RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)， [attribute：：AllowDirectUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
