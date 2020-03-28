---
description: 回复图像格式。 为发送到客户端的图像数据指定图像编码格式，为HTTP响应头指定相应的响应MIME类型。
seo-description: 回复图像格式。 为发送到客户端的图像数据指定图像编码格式，为HTTP响应头指定相应的响应MIME类型。
seo-title: fm
solution: Experience Manager
title: fm
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# fm{#fmt}

回复图像格式。 为发送到客户端的图像数据指定图像编码格式，为HTTP响应头指定相应的响应MIME类型。

` fmt= *`formatpixelTypetiffCompression`*[,[ *``*][, *``*`]

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
  <td class="stentry"> <p>无损PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>具有alpha渠道的无损PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>带有Alpha渠道的TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>嵌入到Macromedia swf文件中的有损JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>有损JPEG和嵌入到Macromedia swf文件中的压缩减缩蒙版。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>嵌入PDF中的图像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>未压缩的二进制封装PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色的GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色的GIF加上主色透明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
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
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
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
  <td class="stentry"> <p>“Deflate”压缩（无损）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG压缩（有损）。 </p> </td> 
 </tr> 
</table>

*`pixelType`* 不指定时效果输出色彩 `icc=` 空间转换；将应用与之对应的默认颜 *`pixelType`* 色用户档案。 如果禁用颜色管理，则应用天真的转换。 *`pixelType`* 指定时将忽 `icc=` 略，这将决定输出像素类型。

*`compression`* 仅当将tif、tif-alpha或PDF指定为 *`format`*&#x200B;有关这些图像格式支持的压缩选项，请参阅下表。

`qlt-` 为以下格式设置JPEG编码选项：JPEG、TIFF（带JPEG压缩）、PDF（带JPEG压缩）和SWF文件。 使用 `quantize=` if `fmt=gif` 或 `fmt=gif-alpha`。 有关详细信息，请参阅命令说明。 其他格式没有可设置的选项。

对于所有格式和像素类型，返回8位／像素组件。

下表列表了有效的组合 *`format`* 和 *`pixelType`*、相应的HTTP响应MIME类型、是否可以嵌入ICC用户档案(请参阅 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f))以及可以应用哪些格式特定的选项命令。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 格式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>响应MIME类型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC用户档案 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg),pathEmbed=, qlt </span> </p> <p>(除 <span class="codeph"> 非tiffCompression设 </span><span class="varname"></span> 置为“jpeg”，否则将忽略qlt=。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf,swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p>(Flash Player忽略嵌入的ICC用户档案。) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>，属 <span class="codeph"> 性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> (除 <span class="codeph"> 非tiffCompression设 </span><span class="varname"></span> 置为“jpeg”，否则将忽略qlt=。) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>（转换为灰色或rgb后，数据将转换为调色板。） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

为发送到客户端的回复图像数据指定编码格式，为HTTP回复头指定相应的响应MIME类型。

`png-alpha` 返回非关联的Alpha（即，Alpha不会预乘像素值），而 `tif-alpha`且 `swf-alpha` 返回关联的Alpha（即，Alpha值与Alpha值预乘）。 Alpha渠道与暗角的背景遮罩的逆对应 `req=img`，并且与组或对象遮罩对应，以防万一 `req=object`。 要在使用嵌套的IR请求时应用Alpha，请 `fmt=` 向嵌入的IR请求和主请求添加相应的Alpha文件格式。 如果使用指定了CMYK或灰度ICC用户档案，则不返回Alpha数据 `icc=`。

## 属性 {#section-eb12a82c69d84622bcea153dd84d95b3}

可能在请求中的任何位置发生。

## 默认 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 默认值 `attribute::Format`为 *`tiffCompression`* ，默认值为 `attribute::TiffEncoding`。 *`pixelType`* 如果未 `rgb` 指 `icc=` 定，则默认为，否则它对应于指定ICC用户档案的像素类型。

## 另请参阅 {#section-c55efc881fc94c70bff91b870e026a7b}

[属性：::](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [属性：JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [属性：:TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qiccIcc](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)[=imbed path,EmbedPath=Ormat,ReqReq=embed=embedChast=ChastingReq=Req,Quintadustivantitud=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
