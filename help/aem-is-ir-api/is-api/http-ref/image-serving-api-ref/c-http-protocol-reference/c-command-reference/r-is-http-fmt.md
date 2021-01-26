---
description: 响应图像格式。
seo-description: 响应图像格式。
seo-title: fm
solution: Experience Manager
title: fm
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 4%

---


# fmt{#fmt}

响应图像格式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alpha | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | 说明 |
|---|---| 
| `jpeg` | 有损JPEG |
| `jpg` | 有损JPG |
| `pjpeg` | 渐进式 JPEG |
| `png` | 24位无损PNG |
| `png8` | 8位无损PNG |
| `png-alpha` | 带alpha渠道的24位无损PNG |
| `png8-alpha` | 带有alpha渠道的8位无损PNG |
| `tif` | TIFF |
| `tif-alpha` | 带Alpha渠道的TIFF |
| `pdf` | 嵌入PDF中的图像 |
| `eps` | 未压缩的二进制封装PostScript |
| `gif` | 2到256色的GIF |
| `gif-alpha` | 具有2到255种颜色加上主色透明度的GIF |
| `swf` | 嵌入到AdobeAS2 swf文件中的有损JPEG |
| `swf-alpha` | 有损JPEG和嵌入到AdobeAS2 swf文件中的平移压缩蒙版 |
| `swf3` | 嵌入到AdobeAS3 swf文件中的有损JPEG |
| `swf3-alpha` | 有损JPEG和嵌入到AdobeAS3 swf文件中的压缩减缩蒙版。 **注意**:swf和swf-alpha格式最适用于ActionScript2应用程序(Flash Player8及更早版本)。建议将swf3和swf3-alpha用于ActionScript3应用程序(Flash Player9和更高版本) |
| `m3u8` | Apple Streaming Server清单格式 |
| `f4m` | Flash流服务器清单格式 |
| `webp` | 有损和无损WebP |
| `webp-alpha` | 具有alpha渠道的有损和无损WebP |
| `jpeg2000` | 有损和无损JPEG 2000 |
| `jpeg2000-alpha` | 具有alpha渠道的有损和无损JPEG 2000 |
| `jpegxr` | 有损和无损JPEG XR |
| `jpegxr-alpha` | 具有alpha渠道的有损和无损JPEG XR |


| *`pixelType`* — rgb | 灰 | cmy |
| *`pixelType`* | 说明 |
|---|---|
| `rgb` | 返回RGB图像数据。 |
| `gray` | 返回灰度图像数据。 |
| `cmyk` | 返回CMYK图像数据。 |

| *`compression`* — none | lzw | zip | jpeg | 有损 | 无损 |
| *`compression`* | 说明 |
|---|---|
| `none` | 未压缩 |
| `lzw` | LZW(Lempel-Ziv-Welch)压缩（无损） |
| `zip` | “Deflate”压缩（无损） |
| `jpeg` | JPEG压缩（有损） |
| `lossy` | WebP、JPEG 2000和JPEG XR压缩（有损） |
| `lossless` | WebP、JPEG 2000和JPEG XR压缩（无损） |

* *`format`* 为发送到客户端的图像数据指定图像编码格式，为HTTP响应头指定相应的响应MIME类型。
* *`pixelType`* 可用于在未指定时实现输出色 `icc=` 彩空间转换。

   将应用与&#x200B;*`pixelType`*&#x200B;对应的默认颜色用户档案。 如果禁用颜色管理，则应用天真的转换。 *`pixelType`* 当指定时 `icc=` 将忽略，这将确定输出像素类型。

* *`compression`* 仅当指定为、 、 、 、 、 、  `tif` 、  `tif-alpha` 、  `pdf` 、  `webp` 、  `webp-alpha`时， `jpeg2000` `jpeg2000-alpha` `jpegxr` `jpegxr-alpha`  *`format`*&#x200B;才允许使用。有关这些图像格式支持的压缩选项，请参阅下表。

可以使用`qlt=`为以下格式设置JPEG编码选项：JPEG、带JPEG压缩的TIFF、带JPEG压缩的PDF和SWF。 WebP、JPEG 2000和JPEG XR也使用`qlt=`，但这些值会对不同格式产生不同的质量。 如果`fmt=gif`或`fmt=gif-alpha`，请使用`quantize=`。 有关详细信息，请参阅命令说明。 其他格式没有可设置的选项。

为所有&#x200B;*`formats`*&#x200B;和&#x200B;*`pixelTypes`*&#x200B;返回每像素8位（GIF为每像素8位）。

下表列表了*`format`*和&#x200B;*`pixelType`*&#x200B;的有效组合、相应的HTTP响应MIME类型、是否可以嵌入ICC用户档案（请参阅[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)）以及可以应用哪些格式特定选项。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 格式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 响应MIME类型</b> </th> 
   <th class="entry"> <b>嵌入ICC用户档案</b> </th> 
   <th class="entry"> <b> 选项</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span>参数仅适用于pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩  </span> </span> <p> (<span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>仅限“tiff”;“tiff-alpha”不支持jpeg压缩。 </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> 除非将 </span> 压缩设 <span class="varname"> 置为 </span> jpeg，否则将忽略 <span class="codeph"> qlt= </span>。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3,swf-alpha,swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意： AdobeFlash Player会忽略嵌入的ICC用户档案。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=, </span>属 <span class="codeph"> 性：:TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 压缩  </span> </span> <p> (<span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 除非将 </span> 压缩设 <span class="codeph"> <span class="varname"> 置为 </span> </span> jpeg，否则将忽略 <span class="codeph"> qlt= </span>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>转换为灰色或rgb后，数据将转换为调色板。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 数量=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 压 </span> </span> 缩( <span class="codeph"> 有损 </span>、无 <span class="codeph"> 损 </span>) </p> <p> <span class="codeph"> 对于 </span> 无损，忽略 <span class="codeph"> qlt= </span>。 </p> <p>由于没有使用WebP格式进行色度缩减采样的概念，因此，如果使用第二个值（如<span class="codeph"> qlt </span>, <span class="codeph"> qlt=80,1 </span>），则忽略第二个值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>与上面一样。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>与上面一样。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

请求属性。 在`req=img`（默认值）或`req=mask`下，无论当前图层设置如何，均适用；否则忽略。

*`type`* 如果指定， `iccProfile=` 则忽略。

## 默认 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`，其 *`defaultType`* 中按如下方式处理：如 `icc=` 果指定， *`defaultType`* 则与指定ICC用户档案的像素类型相对应。如果未指定`icc=`，则&#x200B;*`defaultType`*&#x200B;为`gray`（如果为`req=mask`），否则为`rgb`。

## 示例 {#section-b93222e652df404a84c69025247f07df}

**请求JPEG格式的低质量小预览图像（默认）:**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**请求转换为灰度的图像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**使用alpha渠道以无损格式以高分辨率请求同一图像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**请求与灰度TIFF图像相同的图像的alpha渠道:**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用默认ICC用户档案将同一图像转换为cmyk:**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用不同的ICC用户档案将同一图像转换为cmyk，并将用户档案嵌入到TIFF图像中：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**以TIF文件的形式传送此图像，并且无需像素类型转换：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**将图像转换为具有键色透明度的双色调GIF，并强制颜色转换为黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**有损，质量设置为80:**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**使用alpha无损：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**有损，质量设置为80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**使用alpha无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**有损，质量设置为80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**使用alpha无损：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另请参阅 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , quantize= [, req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), iccEmbed [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)iccEmbed=,  path Embed=, 。
