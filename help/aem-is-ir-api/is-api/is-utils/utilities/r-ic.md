---
description: 图像转换实用程序。
solution: Experience Manager
title: 集成电路
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# 集成电路 {#ic}

图像转换实用程序。

`ic`是一个命令行工具，可将图像文件转换为优化的金字塔TIFF格式(PTIFF)。 虽然图像服务可以处理图像而不进行转换，但我们建议将所有大于512x512像素的图像转换为PTIFF。 此转换可确保最佳服务器性能和资源使用率，并最大限度地缩短响应时间。

建议对包含照片内容的PTIFF文件进行JPEG编码（指定`-jpegcompress`）。 计算机生成的内容可从无损压缩（`-deflatecompress`或`-lzwcompress`）中受益。 除非需要进行色彩转换或像素类型转换，否则将JPEG源图像数据传送到PTIFF而不进行解码，以避免质量下降。 在这种情况下，指定的压缩选项仅适用于较低分辨率的金字塔级别。

如果不转换大图像，则不必设置控制要使用多少内存的参数。 但是，如果是，请使用下面描述的`-maxmem`设置再分配`ic`内存。 计算所需内存量的一个好的经验法则是将图像宽度乘以图像高度再乘以通道数。 例如，对于Alpha乘以3的RGB图像，为4。 此外，如果每个组件的通道为16位，而不是8位，则最终结果会翻倍。

## 使用 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>选项</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>命令选项（见下文）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>单个输入图像文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>单输出PTIFF文件（如果与SourceDirectory一起使用，则无效）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>包含输入图像的文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>将输出PTIFF文件写入其中的文件夹。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-36a2dcfa39824d29b69547c432366219}

如果成功，则为0。 如果发生错误，则返回非零值，并将错误详细信息发送到`stderr`。

## 选项 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> — 未压缩</span> </p> </td> 
   <td colname="col2"> <p>请勿压缩输出图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>使用deflate (zip)压缩（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>使用Lempel-Ziv-Welch (LZW)压缩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>使用JPEG编码。 如果<span class="codeph"> <span class="varname"> sourceFile </span> </span>包含alpha数据，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname">质量</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG质量（0-100；默认值为95）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>禁用JPEG色度缩减像素采样（可提高彩色文本和图形的质量）。 这对CMYK或灰度的输出图像没有影响。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname">数量</span>&gt; &lt; <span class="varname">半径</span>&gt; &lt; <span class="varname">阈值</span>&gt; &lt; <span class="varname">单色</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>将钝化蒙版应用于缺采样的金字塔级别。 有关详细信息，请参阅<a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>。 （不适用于全分辨率图像。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>使用源文件中的剪辑路径（如果有）创建关联的Alpha数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>的打印分辨率(dpi)；如果未指定，则<span class="codeph"> srcFile </span>的打印分辨率将复制到<span class="codeph"> <span class="varname"> destFile </span> </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname">模式</span>&gt; &lt; <span class="varname">容差</span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>计算裁切矩形以最小化纯色背景。 如果自动裁切算法会导致整个图像被裁切，则不会输出裁切信息。 </p> <p>要在不转换图像的情况下计算裁切矩形，请指定<span class="codeph"> — 自动裁切</span> （不带<span class="codeph"> — 转换</span>，不带<span class="codeph"> <span class="varname"> destFile）。</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> 指定要使用种子点的图像角。 如果模式为1，则忽略。</p>
   <p><i><b>模式</b></i> - 0 | 1</p>
   <p>设置为0可基于指定角像素的颜色进行裁切；如果alpha数据与源图像相关联，则对预乘颜色数据有效。</p>
   <p>设置为1将根据Alpha数据进行裁切；将忽略边角且0始终为种子值；如果没有Alpha数据与源图像关联，则不会应用裁切。</p> 
   <p><i><b>容差</b></i> — 匹配容差。 实际值0.0到1.0。指定匹配像素组件值的公差。 设置为0表示完全匹配。</p>
   <p><i><b>infoFile</b></i> — 将裁切信息数据写入到的XML输出文件的路径和名称。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>将XMP元数据（如果可用）从<span class="codeph"> <span class="varname"> sourceFile </span> </span>复制到<span class="codeph"> <span class="varname"> destFile </span> </span>，而不进行修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 将ICC颜色配置文件嵌入到<span class="codeph"> <span class="varname"> destFile </span> </span>（如果可用）（默认情况下未嵌入任何配置文件）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname">文件</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置文件文件的路径和名称。 定义<span class="codeph"> <span class="varname"> sourceFile </span> </span>的颜色空间，并且必须匹配其像素类型。 仅当<span class="codeph"> <span class="varname"> sourceFile </span> </span>中没有嵌入配置文件时才应指定，因为这会覆盖嵌入的配置文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname">文件</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置文件文件的路径和名称。 定义<span class="codeph"> <span class="varname"> destFile </span> </span>的像素类型和颜色空间。 如果<span class="codeph"> <span class="varname"> sourceFile </span> </span>具有嵌入配置文件，或者也指定了<span class="codeph"> -imageprofile </span>，则IC将转换为此配置文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>用于色彩空间转换的可感知渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> 用于色彩空间转换的相对比色渲染方法（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>用于色彩空间转换的绝对比色渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>色彩空间转换的饱和度渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>禁用特定颜色转换的黑场补偿 </p> <p>默认启用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>颜色转换时禁用仿色（误差扩散）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> 禁用从CMYK到RGB的自动转换。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>强制对JPEG输入图像进行解码和重新编码。 </p> <p> <b>注意：</b>应用此选项可能会降低图像质量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>使用标准质量（双线性）重新取样过滤器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>使用更高质量（Lanczos窗口）的重新取样过滤器（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>使用更高质量(FlashPix)重新取样滤镜。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>使用Photoshop样式的8x8双三次锐化过滤器缩减采样。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> 当指定为第一个选项时，如果遇到无效选项，将禁止输出使用信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> — 覆盖</span> </p> </td> 
   <td colname="col2"> <p>允许覆盖现有的<span class="codeph"> <span class="varname"> destFile </span> </span>。 默认情况下，会在文件名后附加一个数字后缀，以防止覆盖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>忽略隐藏的源文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>发生错误时不要停止处理。 仅在处理多个文件时有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname">文件</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日志文件的路径和名称（默认为<span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname">级别</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日志级别。 </p> 
   <p>&lt; 0 — 已禁用日志记录。</p>
   <p>0 — 列出要处理的文件。</p>
   <p>1 — 为不需要的文件添加报告。</p>
   <p>2 — 添加进度报告。</p>
   <p>3 — 添加有关遇到的每个文件的报表。</p>
   <p>4 — 在文件级别添加进度报告。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>附加到日志文件（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>覆盖日志文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname">毫秒</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日志级别2和更高级别的日志记录间隔（以毫秒为单位）（默认值为3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname">字节</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>内存使用限制。 必须至少为10 MB。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname">百分比</span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>内存使用限制。 缺省值为物理内存的25%。 如果<span class="codeph"> maxmem </span>和<span class="codeph"> maxmempercent </span>均未显式设置，则使用maxmempercent默认值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> — 版本</span> </p> </td> 
   <td colname="col2"> <p> 返回此实用程序的版本信息。 指定而不使用其他选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支持的输入图像格式 {#section-ab13d941d6724e65b9f84b62d949d31c}

下表列出了IC支持的图像文件格式和格式选项。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b>格式</b> </p> </th> 
   <th class="entry"> <p> <b>像素类型</b> <b>位/Chan</b> </p> </th> 
   <th class="entry"> <p> <b>位/Chan</b> </p> </th> 
   <th class="entry"> <p> <b>压缩</b> </p> </th> 
   <th class="entry"> <p> <b>备注</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows位图） </p> </td> 
   <td> <p> RGB | 已索引 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 未压缩 | RLE </p> </td> 
   <td> <p> 5/6位/通道表示支持16位RGB（5-5-5和5-6-5位/通道）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （封装的Postscript） </p> </td> 
   <td> <p> CMYK | RGB | 灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | 二进制 | JPEG </p> </td> 
   <td> <p> 仅支持由Photoshop生成的EPS文件。 </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> 已索引 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 如果存在，调色板中的透明度值将转换为Alpha。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b>JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | 灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | 灰色 | 灰色A </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未压缩 | 已压缩 </p> </td> 
   <td> <p> 仅合并图像；忽略图层和多余的通道。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 仅位图数据；忽略矢量数据。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | 灰色 | 灰色A | 已索引 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 压缩的 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b>TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | 灰色 | 灰色A | 已索引 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未压缩 | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | 数据包位 </p> </td> 
   <td> <p> 除了第一个关联的Alpha通道外，会忽略其他通道。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以在EPS、JPG、PSD、PNG和TIFF文件中识别嵌入的ICC配置文件。

可以在EPS、JPG、PSD和TIFF文件中识别嵌入路径和XMP元数据。

## 示例 {#section-3c1986b30315431989bd76b1ee5bef6d}

以最佳质量转换单个图像并将其保存在同一文件夹中：

`ic -convert src/myFile.png src/myFile.tif`

将&#x200B;*`srcFolder`*&#x200B;中的所有图像转换为JPEG编码的金字塔TIFF并置于&#x200B;*`destFolder`*&#x200B;中：

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

转换&#x200B;*`srcFolder`*&#x200B;中的所有图像。 JPG文件的编码图像数据用于这些图像的其余图像金字塔以及所有非JPG输入文件的整个输出图像的全分辨率级别、无损LZW压缩。 像素类型、嵌入的颜色配置文件、XMP元数据等。 将进行维护。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
