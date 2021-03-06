---
title: src
description: 材料文件。 以单个材料目录引用的形式指定材料数据，或以逗号分隔的一个或两个图像或材料数据文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# src{#src}

材料文件。 以单个材料目录引用的形式指定材料数据，或以逗号分隔的一个或两个图像或材料数据文件。

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`指数`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rprace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>材料目录ID(<span class="codeph"> 属性：:RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>物料目录条目(<span class="codeph"> 目录：:Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料样式文件(<span class="filepath"> .vnc</span> 或 <span class="filepath"> .vnw</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>图像数据文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>请求图像提供。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>请求图像渲染。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>请求到外部服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的名称。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 指数</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的索引号为0。 </p></td> 
 </tr> 
</table>

可重复的纹理、贴胶和墙纸材料需要单幅图像，该图像可以指定为文件或嵌入请求。

机柜材料需要机柜样式文件( [!DNL .vnc])，不能指定为嵌套请求。 纹理图像文件对于文件柜是可选的，如果指定，则可能是文件或嵌入请求。

窗口覆盖材料需要窗口覆盖样式文件( [!DNL .vnw])，不能指定为嵌套请求。 纹理文件是可选的，如果指定，它可以是文件或嵌入式请求。

图像渲染使用与图像服务相同的规则来查找材料目录、目录条目和数据文件。 请参阅 *`object`* 有关详细信息，请参阅图像提供文档中的数据类型。

*`materialFile`* 是相对于 `attribute::RootPath`.

*`foreignReq`* 可以是相对于 `attribute::RootUrl`，或绝对URL(如果 `attribute::AllowDirectUrls` 设置。

如果 *`catId`* 未指定，则使用会话目录。

`srcE=` 和 `srcN=` 提供对嵌入到晕影中的材料的访问。

## 支持的文件格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

图像渲染支持与Dynamic Media图像服务相同的源图像格式。

使用Scene7金字塔TIFF(PTIFF)多分辨率格式时，需要多种不同分辨率的图像数据的应用程序性能最佳。 图像提供包括图像转换器(IC)实用程序，该实用程序可根据任何支持的格式创建PTIFF图像。

有关支持的文件格式的完整列表，请参阅图像服务文档中IC实用程序的说明。

## 属性 {#section-e68d03788d534e2184147987d51dfd0f}

材料属性。 除纯色外的所有材料（不允许使用纯色材料）均需要此参数。 所有字符串均区分大小写。 *`index`* 必须为0或更大。

## 默认 {#section-dde549c1917540dc8f9555962202da3c}

无。

## 示例 {#section-675865444f8a4d35b9fc6e58b36e3438}

具有独立可重复纹理的彩色机柜的MSS:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

同样的材料可以在材料目录中 `'cat`记录&#39;中的&#39; `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

对“图像提供”的嵌套请求，以获取纹理图像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另请参阅 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[材料目录](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [属性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [属性：:AllowDirectUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
