---
title: src
description: 材料文件。 以单个材质目录引用的形式指定材质数据，或者以逗号分隔的一个或两个图像或材质数据文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# src{#src}

材料文件。 以单个材质目录引用的形式指定材质数据，或者以逗号分隔的一个或两个图像或材质数据文件。

`src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`名称`*`

`srcN= *`索引`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname">材料文件</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;amp；花括号；'is&amp;amp；花括号；'<span class="varname"> isReq</span>'&amp;amp；花括号；'&amp;amp；花括号；|&amp;amp；花括号；'<span class="varname"> irReq</span>'&amp;amp；花括号；'|&amp;amp；花括号；'&amp;amp；花括号；'&amp;amp；花括号；'<span class="varname"> foreignReq</span>'&amp;amp；花括号；'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>材质目录ID （<span class="codeph">属性：：RootId</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>材质目录条目（<span class="codeph">目录：：Id</span>）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>材料样式文件（<span class="filepath"> .vnc</span>或<span class="filepath"> .vnw</span>）。 </p></td> 
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
  <td class="stentry"> <p><span class="varname">名称</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的名称。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">索引</span> </p></td> 
  <td class="stentry"> <p>嵌入材料的从0开始的索引号。 </p></td> 
 </tr> 
</table>

可重复的纹理、贴花和墙纸材料需要单个图像，可以指定为文件或嵌入请求。

CAB材料需要一个CAB样式文件([!DNL .vnc])，该文件不能指定为嵌套请求。 纹理图像文件对于文件柜是可选的，如果指定，它可以是一个文件，也可以是一个嵌入的请求。

窗口覆盖材料需要窗口覆盖样式文件([!DNL .vnw])，该文件不能指定为嵌套请求。 纹理文件是可选的，如果指定，它可以是一个文件，也可以是一个嵌入的请求。

图像渲染使用与图像服务相同的规则来查找材料目录、目录条目和数据文件。 有关详细信息，请参阅图像服务文档中&#x200B;*`object`*&#x200B;数据类型的描述。

*`materialFile`*&#x200B;是`attribute::RootPath`的相对路径。

*`foreignReq`*&#x200B;可以是相对于`attribute::RootUrl`的URL，也可以是绝对的URL（如果已设置`attribute::AllowDirectUrls`）。

如果未指定&#x200B;*`catId`*，则使用会话目录。

`srcE=`和`srcN=`提供对晕影中嵌入的材料的访问权限。

## 支持的文件格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

图像渲染支持与Dynamic Media图像服务相同的源图像格式。

当使用Scene7金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 图像服务包括从任何支持的格式创建PTIFF图像的图像转换器(IC)实用程序。

有关支持的文件格式的完整列表，请参阅图像服务文档中的IC实用程序描述。

## 属性 {#section-e68d03788d534e2184147987d51dfd0f}

材质属性。 除纯色以外的所有材料均需要（纯色材料不允许使用）。 所有字符串都区分大小写。 *`index`*&#x200B;必须大于或等于0。

## 默认 {#section-dde549c1917540dc8f9555962202da3c}

无。

## 示例 {#section-675865444f8a4d35b9fc6e58b36e3438}

用于具有单独可重复纹理的彩色机柜的MSS：

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

记录“`12-3-2`”中的材质目录`'cat`中可以存在相同的材质：

`…&obj=cabinets&src=cat/12-3-2&…`

对图像服务的嵌套请求以获取纹理图像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另请参阅 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[材料目录](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)，[属性：：RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)，[属性：：AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
