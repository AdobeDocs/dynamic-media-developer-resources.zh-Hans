---
description: 回复图像格式。 为发送到客户端的图像数据指定图像编码格式，并为HTTP响应标头指定相应的响应MIME类型。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 4%

---

# fmt{#fmt}

回复图像格式。 为发送到客户端的图像数据指定图像编码格式，并为HTTP响应标头指定相应的响应MIME类型。

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 格式 </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>有损JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>有损JPG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>无丢失的PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>带Alpha通道的无丢失PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-α </p> </td> 
  <td class="stentry"> <p>带有Alpha通道的TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>嵌入到Macromedia swf文件中的有损JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>有损JPEG和嵌入到Macromedia swf文件中的通缩压缩蒙版。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>PDF中嵌入的图像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>未压缩的二进制封装的PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色加键色透明度的GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>返回RGB图像数据。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>灰色 </p> </td> 
  <td class="stentry"> <p>返回灰度图像数据。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmy </p> </td> 
  <td class="stentry"> <p>返回CMYK图像数据。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>无 </p> </td> 
  <td class="stentry"> <p>未压缩. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW(Lempel-Ziv-Welch)压缩（无损）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>“缩减”压缩（无损）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG压缩（有损）。 </p> </td> 
 </tr> 
</table>

*`pixelType`* 未指定时，影响输出色 `icc=` 彩空间转换；将应用与对应的默认颜色配 *`pixelType`* 置文件。如果禁用色彩管理，则应用天真的转换。 *`pixelType`* 在指定时将 `icc=` 忽略，这将确定输出像素类型。

*`compression`* 仅当将tif、tif-alpha或PDF指定为时，才允许使用 *`format`*。有关这些图像格式支持的压缩选项，请参阅下表。

`qlt-` 为以下格式设置JPEG编码选项：JPEG、带有JPEG压缩的TIFF、带有JPEG压缩的PDF和SWF文件。如果为`fmt=gif`或`fmt=gif-alpha`，则使用`quantize=`。 有关详细信息，请参阅命令描述。 其他格式没有可设置的选项。

对于所有格式和像素类型，每像素组件返回八位。

下表列出了&#x200B;*`format`*&#x200B;和&#x200B;*`pixelType`*&#x200B;的有效组合、相应的HTTP响应MIME类型、是否可以嵌入ICC配置文件（请参阅[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)），以及可以应用哪些特定于格式的选项命令。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 格式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>响应MIME类型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC配置文件 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg，jpg </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png， png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif， tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> （无|lzw|zip|jpeg）， pathEmbed=, qlt  </span> </p> <p>（除非将<span class="codeph"> qlt= </span>设置为“jpeg”，否则将忽略<span class="varname"> tiffCompression </span>。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf，swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p>(Flash Player会忽略嵌入的ICC配置文件。) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>, <span class="codeph"> 属性：:TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> （无|zip|jpeg），qlt=  </span> </p> <p> （除非将<span class="codeph"> qlt= </span>设置为“jpeg”，否则将忽略<span class="varname"> tiffCompression </span>。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif，gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>（数据在转换为灰色或rgb后会转换为调色板。） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

为发送到客户端的回复图像数据指定编码格式，并为HTTP回复标头指定相应的响应MIME类型。

`png-alpha` 返回未关联的alpha（即，alpha不会预乘像素值），而 `tif-alpha`返回 `swf-alpha` 关联的alpha（即，alpha值与alpha值预乘）。Alpha通道对应于晕影的`req=img`背景掩码的反像；如果存在`req=object`，则对应于组或对象掩码。 要在使用嵌套IR请求时应用Alpha，请向嵌入的IR请求和主请求中添加具有相应Alpha文件格式的`fmt=`。 如果使用`icc=`指定CMYK或灰度ICC配置文件，则不返回Alpha数据。

## 属性 {#section-eb12a82c69d84622bcea153dd84d95b3}

可以在请求中的任意位置发生。

## 默认 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 默认值 `attribute::Format`为， *`tiffCompression`* 默认值 `attribute::TiffEncoding`为。*`pixelType`* 如果未指 `rgb` 定 `icc=` ，则默认为，否则，它对应于指定ICC配置文件的像素类型。

## 另请参阅 {#section-c55efc881fc94c70bff91b870e026a7b}

[属性：:Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f),  [请求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb),  [Quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
