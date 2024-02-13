---
title: 格式
description: 响应图像格式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 9ed415c5ab4444a2d404782bfd96ded3c47c26cd
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 2%

---

# 格式{#fmt}

响应图像格式。

`fmt=format[,` `[`*`pixelType`*`]`，`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 说明 |
|---|---|
| `avif-alpha` | 带有Alpha通道的有损无损AVIF。 |
| `avif` | 有损、无损的AVIF。 |
| `eps` | 未压缩的二进制封装的PostScript。 |
| `f4m` | Streaming Server清单格式Flash。 |
| `gif-alpha` | 2到255色GIF加上键色透明度。 |
| `gif` | GIF为2到256色。 |
| `heic` | 无损HEIC。 如果不支持此格式，则默认从浏览器下载。 |
| `jpeg` | JPEG有损。 |
| `jpeg2000-alpha` | 具有Alpha通道的有损和无损JPEG2000。 |
| `jpeg2000` | 有损和无损JPEG2000。 |
| `jpegxr-alpha` | 带Alpha通道的有损无损JPEGXR。 |
| `jpegxr` | 有损无损JPEGXR。 |
| `jpg` | JPG有损。 |
| `m3u8` | Apple流服务器清单格式。 |
| `pdf` | 嵌入到PDF中的图像。 |
| `pjpeg` | 渐进式JPEG。 |
| `png-alpha` | 带有Alpha通道的24位无损PNG。 |
| `png` | 24位无损PNG。 |
| `png8-alpha` | 带有Alpha通道的8位无损PNG。 |
| `png8` | 8位无损PNG。 |
| `swf-alpha` | 嵌入到AdobeAS2 swf文件中的有损JPEG和Deflate-Compressed掩码。 |
| `swf` | 嵌入到AdobeAS2 swf文件中的有损JPEG。 |
| `swf3-alpha` | 嵌入到AdobeAS3 swf文件中的有损JPEG和Deflate-Compressed掩码。 **注意：** swf和swf-alpha格式最适合ActionScript2应用程序(Flash Player8及更早版本)。 建议将swf3和swf3-alpha格式用于ActionScript3应用程序(Flash Player9及更高版本)。 |
| `swf3` | 嵌入到AdobeAS3 swf文件中的有损JPEG。 |
| `tif-alpha` | 带有Alpha通道的TIFF。 |
| `tif` | TIFF。 |
| `webp-alpha` | 带有Alpha通道的有损无损WebP。 |
| `webp` | 有损无损WebP。 |

| *`pixelType`* - rgb | 灰色 | cmyk |
| *`pixelType`* | 说明 |
|---|---|
| `cmyk` | 返回CMYK图像数据。 |
| `gray` | 返回灰度图像数据。 |
| `rgb` | 返回RGB图像数据。 |

| *`compression`* - jpeg | 有损 | 无损 | lzw | 无 | zip |
| *`compression`* | 说明 |
|---|---|
| `jpeg` | JPEG压缩（有损）。 |
| `lossy` | WebP、JPEG2000和JPEGXR压缩（有损）。 |
| `lossless` | WebP、JPEG2000和JPEGXR（无损）。 |
| `lzw` | LZW (Lempel-Ziv-Welch)压缩（无损）。 |
| `none` | 未压缩。 |
| `zip` | “Deflate”压缩（无损）。 |

* *`format`* 指定发送到客户端的图像数据的图像编码格式以及HTTP响应标头对应的响应MIME类型。
* *`pixelType`* 可以在以下情况下用于实现输出色彩空间转换 `icc=` 未指定。

  与对应的默认颜色配置文件 *`pixelType`* 中所有规则都适用的URL的区域。 如果禁用颜色管理，则应用朴素转换。 *`pixelType`* 被忽略的时间 `icc=` 指定，它确定输出像素类型。

* *`compression`* 仅在 `tif`， `tif-alpha`， `pdf`， `webp`， `webp-alpha`， `jpeg2000`， `jpeg2000-alpha`， `jpegxr`，或 `jpegxr-alpha` 指定为 *`format`*. 有关这些图像格式支持的压缩选项，请参阅下表。

您可以使用 `qlt=` 为以下格式设置JPEG编码选项：JPEG、使用JPEG压缩的TIFF、使用JPEG压缩的PDF和SWF。 WebP、JPEG2000和JPEGXR也使用 `qlt=` 但是这些值会根据不同的格式产生不同的品质。 使用 `quantize=` 如果 `fmt=gif` 或 `fmt=gif-alpha`. 有关详细信息，请参阅命令说明。 其他格式没有可设置的选项。

对于所有像素，每像素组件返回8位 *`formats`* 和 *`pixelTypes`* (GIF每像素8位)。

下表列出了*的有效组合`format`*和 *`pixelType`*，相应的HTTP响应MIME类型，是否可以嵌入ICC配置文件(请参阅 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e))，以及可以应用的特定于格式的选项。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 格式</i> </b> </th> 
   <th class="entry"> <b> <i> 像素类型</i> </b> </th> 
   <th class="entry"> <b> 响应MIME类型</b> </th> 
   <th class="entry"> <b>嵌入ICC配置文件</b> </th> 
   <th class="entry"> <b> 选项</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg， jpg， pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、灰度、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>， <span class="codeph"> pscan= </span>， <span class="codeph"> qlt= </span>， <span class="codeph"> xmpEmbed= </span> </p> <p>此 <span class="codeph"> pscan= </span> 参数仅适用于pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png， png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰度 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8， png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif， tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、灰度、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩 </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>仅限“tiff”；“tiff-alpha”不支持jpeg压缩。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 被忽略，除非 <span class="varname"> 压缩 </span> 设置为 <span class="codeph"> jpeg </span>. </p> <p>， pathEmbed=， xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf，swf3， swf-alpha， swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰度 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意：AdobeFlash Player会忽略嵌入的ICC配置文件。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>， <span class="codeph"> 属性：：TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb、灰度、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩 </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>)， <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 被忽略，除非 <span class="codeph"> <span class="varname"> 压缩 </span> </span> 设置为 <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、灰度、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif， gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰度 </p> <p>数据在转换为灰色或rgb后转换为调色板。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 量化= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp， webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 压缩 </span> </span> ( <span class="codeph"> 有损 </span>， <span class="codeph"> 无损 </span>) </p> <p> <span class="codeph"> qlt= </span> 被忽略 <span class="codeph"> 无损 </span>. </p> <p>由于没有使用WebP格式进行色度缩减像素采样的概念，因此如果您使用第二个值 <span class="codeph"> qlt </span> (例如， <span class="codeph"> qlt=80,1 </span>)第二个值( <span class="codeph"> 1 </span>)将被忽略。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000， jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰度 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>同上。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr， jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>同上。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif，avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>同上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

请求属性。 无论当前图层设置如何，在以下情况下均适用： `req=img` （默认）或 `req=mask`；否则忽略。

*`type`* 忽略以下情况 `iccProfile=` 已指定。

## 默认 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`默认类型`*,none`，其中 *`defaultType`* 按以下方式处理：如果 `icc=` 已指定， *`defaultType`* 对应于指定ICC配置文件的像素类型。 如果 `icc=` 未指定， *`defaultType`* 是 `gray` 如果 `req=mask`，否则为 `rgb`.

## 示例 {#section-b93222e652df404a84c69025247f07df}

**请求JPEG格式的低质量小型预览图像（默认）：**

` http:// *`服务器`*/myRootId/myImageId?qlt=60&wid=200`

**请求将相同的图像转换为灰度：**

` http:// *`服务器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**请以Alpha通道的无损失格式和高分辨率请求相同的图像：**

` http:// *`服务器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**请求将同一图像作为灰度TIFF图像的Alpha通道：**

` http:// *`服务器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用默认ICC配置文件将同一图像转换为cmyk：**

` http:// *`服务器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用其他ICC配置文件将同一图像转换为cmyk，并将配置文件嵌入到TIFF图像中：**

` http:// *`服务器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**将此图像作为TIF文件传递，无需转换像素类型即可进行JPEG压缩：**

` http:// *`服务器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**将图像转换为具有键色透明度的双调GIF，并强制将颜色转换为黑白色：**

` http:// *`服务器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**质量设置为80时为有损：**

` http:// *`服务器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**带有Alpha的无损：**

` http:// *`服务器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**质量设置为80时为有损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**带有Alpha的无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**质量设置为80时为有损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**带有Alpha的无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另请参阅 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [量化=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)， [需要=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)， [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)， [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)， [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
