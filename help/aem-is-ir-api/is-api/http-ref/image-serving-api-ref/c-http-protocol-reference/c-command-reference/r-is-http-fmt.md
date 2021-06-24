---
description: 响应图像格式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 07490c6169511f824f0c0d75ef2d692ac816858e
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 4%

---

# fmt{#fmt}

响应图像格式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha |swf |swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 说明 |
|---|---|
| `avif-alpha` | 具有Alpha通道的有损和无损AVIF <br><br>*此格式的发布时间表：* <br><b>北美</b> — 现已推出<br><b>欧洲、中东、非洲</b> - 2021年8月13日<br><b>亚太</b> - 2021年6月29日 |
| `avif` | 有损和无损的AVIF <br><br>*此格式的发布时间表：*<br><b>&#x200B;北美</b> — 现已推出<br><b>欧洲、中东、非洲</b> - 2021年8月13日<br><b>亚太</b> - 2021年6月29日 |
| `eps` | 未压缩的二进制封装的PostScript |
| `f4m` | Flash流服务器清单格式 |
| `gif-alpha` | 2到255色加上键色透明度的GIF |
| `gif` | 2到256色的GIF |
| `jpeg` | 有损JPEG |
| `jpeg2000-alpha` | 带Alpha通道的有损和无损JPEG 2000 |
| `jpeg2000` | 有损和无损JPEG 2000 |
| `jpegxr-alpha` | 带Alpha通道的有损和无损JPEG XR |
| `jpegxr` | 有损和无损JPEG XR |
| `jpg` | 有损JPG |
| `m3u8` | Apple流服务器清单格式 |
| `pdf` | PDF中嵌入的图像 |
| `pjpeg` | 渐进式 JPEG |
| `png-alpha` | 带Alpha通道的24位无损PNG |
| `png` | 24位无损PNG |
| `png8-alpha` | 带Alpha通道的8位无损PNG |
| `png8` | 8位无损PNG |
| `swf-alpha` | 有损JPEG和嵌入到AdobeAS2 swf文件中的通缩压缩蒙版 |
| `swf` | 嵌入到AdobeAS2 swf文件中的有损JPEG |
| `swf3-alpha` | 有损JPEG和嵌入到AdobeAS3 swf文件中的通缩压缩蒙版。 **注意：** swf和swf-alpha格式最适用于ActionScript2应用程序(Flash Player8及更早版本)。建议使用swf3和swf3-alpha格式来ActionScript3应用程序(Flash Player9及更高版本) |
| `swf3` | 嵌入到AdobeAS3 swf文件中的有损JPEG |
| `tif-alpha` | 带Alpha通道的TIFF |
| `tif` | TIFF |
| `webp-alpha` | 带Alpha通道的有损和无损WebP |
| `webp` | 有损和无损WebP |

| *`pixelType`* – rgb | 灰色 | cmy |
| *`pixelType`* | 说明 |
|---|---|
| `cmyk` | 返回CMYK图像数据。 |
| `gray` | 返回灰度图像数据。 |
| `rgb` | 返回RGB图像数据。 |

| *`compression`* – none | lzw | zip | jpeg | 有损 | 无损 |
| *`compression`* | 说明 |
|---|---|
| `jpeg` | JPEG压缩（有损） |
| `lossy` | WebP、JPEG 2000和JPEG XR压缩（有损） |
| `lossless` | WebP、JPEG 2000和JPEG XR压缩（无损） |
| `lzw` | LZW(Lempel-Ziv-Welch)压缩（无损） |
| `none` | 未压缩 |
| `zip` | “缩减”压缩（无损） |

* *`format`* 为发送到客户端的图像数据指定图像编码格式，为HTTP响应标头指定相应的响应MIME类型。
* *`pixelType`* 可用于在未指定时实现输出色 `icc=` 彩空间转换。

   将应用与&#x200B;*`pixelType`*&#x200B;对应的默认颜色配置文件。 如果禁用色彩管理，则应用天真的转换。 *`pixelType`* 在指定时将 `icc=` 忽略，这将确定输出像素类型。

* *`compression`* 仅当将 `tif`、  `tif-alpha`、  `pdf`、  `webp`、  `webp-alpha`、  `jpeg2000`、  `jpeg2000-alpha` `jpegxr`或 `jpegxr-alpha` 指定为 *`format`*&#x200B;时，才允许使用。有关这些图像格式支持的压缩选项，请参阅下表。

可以使用`qlt=`为以下格式设置JPEG编码选项：JPEG、带JPEG压缩的TIFF、带JPEG压缩的PDF和SWF。 WebP、JPEG 2000和JPEG XR也使用`qlt=`，但值会导致不同格式的质量不同。 如果为`fmt=gif`或`fmt=gif-alpha`，则使用`quantize=`。 有关详细信息，请参阅命令描述。 其他格式没有可设置的选项。

为所有&#x200B;*`formats`*&#x200B;和&#x200B;*`pixelTypes`*&#x200B;返回每像素8位的组件（GIF为每像素8位）。

下表列出了*`format`*和&#x200B;*`pixelType`*&#x200B;的有效组合、相应的HTTP响应MIME类型、是否可以嵌入ICC配置文件（请参阅[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)），以及可以应用的特定于格式的选项。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 格式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 响应MIME类型</b> </th> 
   <th class="entry"> <b>嵌入ICC配置文件</b> </th> 
   <th class="entry"> <b> 选项</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg， jpg， pjpeg </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span>参数仅适用于pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png， png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif， tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩  </span> </span> <p> （<span class="codeph">无|lzw|zip|jpeg </span>） </p> <p>仅“tiff”；“tiff-alpha”不支持jpeg压缩。 </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> 除非将 </span> 压缩设置 <span class="varname"> 为 </span> jpeg，否则将 <span class="codeph"> 忽略qlt </span>= </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf，swf3,swf-alpha，swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意： AdobeFlash Player会忽略嵌入的ICC配置文件。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>, <span class="codeph"> 属性：:TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩  </span> </span> <p> （<span class="codeph">无|zip|jpeg </span>, <span class="codeph"> qlt= </span>） </p> <p> <span class="codeph"> 除非将 </span> 压缩设置 <span class="codeph"> <span class="varname"> 为 </span> </span> jpeg，否则将 <span class="codeph"> 忽略qlt </span>= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif，gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>数据在转换为灰色或rgb后会转换为调色板。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 数量=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp、webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 压 </span> </span> 缩( <span class="codeph"> 有损 </span>、无 <span class="codeph"> 损 </span>) </p> <p> <span class="codeph"> qlt=会 </span> 忽略无 <span class="codeph"> 损 </span>。 </p> <p>由于没有使用WebP格式进行色度缩减采样的概念，因此如果使用第二个值，其中<span class="codeph"> qlt </span>（例如，<span class="codeph"> qlt=80,1 </span>），则忽略第二个值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>与上文相同。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr， jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>与上文相同。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> 阿维夫、阿维夫 — 阿尔法 </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>与上文相同。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

请求属性。 在`req=img`（默认）或`req=mask`下，无论当前层设置如何，均适用；否则将忽略。

*`type`* 如果指定， `iccProfile=` 则忽略。

## 默认 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`，其中 *`defaultType`* 的处理方式如下：如果 `icc=` 指定，则对 *`defaultType`* 应于指定ICC配置文件的像素类型。如果未指定`icc=`，则&#x200B;*`defaultType`*&#x200B;为`gray`（如果为`req=mask`），否则为`rgb`。

## 示例 {#section-b93222e652df404a84c69025247f07df}

**请求JPEG格式的低质量小预览图像（默认）：**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**请求转换为灰度的相同图像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**使用Alpha通道以无损格式以高分辨率请求同一图像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**为与灰度级TIFF图像相同的图像请求Alpha通道：**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用默认ICC配置文件将同一图像转换为cmyk:**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用不同的ICC配置文件将同一图像转换为cmyk，并将配置文件嵌入到TIFF图像中：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**将此图像作为TIF文件传送，并在不进行像素类型转换的情况下进行JPEG压缩：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**将图像转换为具有键色透明度的双色调GIF，并强制将颜色转换为黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**质量设置为80有损：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**使用Alpha进行无损：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**质量设置为80有损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**使用Alpha进行无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**质量设置为80有损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**使用Alpha进行无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另请参阅 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301),  [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
