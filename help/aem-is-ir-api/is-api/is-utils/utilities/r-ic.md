---
description: 图像转换实用程序。
seo-description: 图像转换实用程序。
seo-title: ic
solution: Experience Manager
title: ic
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 2%

---


# ic {#ic}

图像转换实用程序。

`ic` 是一种命令行工具，可将图像文件转换为优化的金字塔TIFF格式(PTIFF)。虽然图像服务可以处理图像而无需转换，但建议您将所有大于512x512像素的图像转换为PTIFF。 此转换可确保最佳服务器性能和资源使用并最大限度地缩短响应时间。

建议对包含照片内容的PTIFF文件进行JPEG编码（指定`-jpegcompress`）。 计算机生成的内容可以从无损压缩（`-deflatecompress`或`-lzwcompress`）中受益。 除非需要颜色转换或像素类型转换，否则JPEG源图像数据将在不进行解码的情况下传输到PTIFF，以避免质量下降。 在这种情况下，指定的压缩选项仅适用于低分辨率金字塔级。

如果不转换大图像，则不必设置控制要使用多少内存的参数。 但是，如果您是，请使用下面描述的`-maxmem`设置为`ic`增加内存。 计算所需内存量的一个好经验法则是将图像的宽度乘以图像的高度乘以渠道数。 例如，对于alpha乘以3的RGB图像，4表示。 此外，如果渠道为16位／分量，而不是8多次最终结果。

## 使用 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>选项</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>命令选项（请参阅下文）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>单个输入图像文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>单个输出PTIFF文件（如果与SourceDirectory一起使用，则无效）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>包含输入图像的文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>将输出PTIFF文件写入到的文件夹。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-36a2dcfa39824d29b69547c432366219}

0（如果成功）。 如果发生错误，则返回一个非零值，并将错误详细信息发送到`stderr`。

## 选项 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未压缩的 </span> </p> </td> 
   <td colname="col2"> <p>不要压缩输出图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflate compress  </span> </p> </td> 
   <td colname="col2"> <p>使用deflate(zip)压缩（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>使用Lempel-Ziv-Welch(LZW)压缩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>使用JPEG编码。 如果<span class="codeph"> <span class="varname"> sourceFile </span> </span>包含alpha数据，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>JPEG质量(0-100;默认值为95)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance  </span> </p> </td> 
   <td colname="col2"> <p>禁用JPEG色度缩减采样（可提高颜色文本和图形的质量）。 这对CMYK或灰度的输出图像没有影响。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span> &lt;&gt; &gt;  </span>monochrome &gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>将USM锐化应用于次采样金字塔级。 有关详细信息，请参阅<a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>。 （未应用于全分辨率图像。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>使用源文件中的剪辑路径（如果有）创建关联的alpha数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>的打印分辨率(dpi);如果未指定，则将<span class="codeph"> srcFile </span>的打印分辨率复制到<span class="codeph"> <span class="varname"> destFile </span> </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode tolerance  </span>&gt;  &lt;&gt;  </span> &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>计算裁剪矩形以最小化纯色背景。 如果自动裁剪算法会导致整个图像被裁剪，则不会输出裁剪信息。 </p> <p>要计算裁剪矩形而不转换图像，请指定<span class="codeph"> -autocrop </span>（不带<span class="codeph"> -convert </span>）和<span class="codeph"> <span class="varname"> destFile。</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> 指定要使用种子点的图像的哪个角。 如果模式为1，则忽略。</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>设置为0可基于指定角像素的颜色进行裁剪；如果alpha数据与源图像关联，则可处理预乘颜色数据。</p>
   <p>设置为1可基于alpha数据进行裁剪；corner被忽略，0始终为种子值；如果没有与源图像关联的alpha数据，则不应用任何裁剪。</p> 
   <p><i><b>容差</b></i> -匹配容差。实数值0.0到1.0。指定匹配像素组件值的容差。 为精确匹配设置0。</p>
   <p><i><b>infoFile</b></i>  —— 要向其写入裁剪信息数据的XML输出文件的路径和名称。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>如果有XMP元数据可用，请将元数据从<span class="codeph"> <span class="varname"> sourceFile </span> </span>复制到<span class="codeph"> <span class="varname"> destFile </span> </span> ，无需修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> 在<span class="codeph"> <span class="varname"> destFile </span> </span>中嵌入ICC颜色用户档案（如果可用）(默认情况下不嵌入用户档案)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt;&gt; 文件 </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICC用户档案文件的路径和名称。 定义<span class="codeph"> <span class="varname"> sourceFile </span> </span>的色彩空间，并且必须与其像素类型匹配。 仅当<span class="codeph"> <span class="varname"> sourceFile </span> </span>中未嵌入用户档案时，才应指定该用户档案，因为这将覆盖嵌入的。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt;&gt; 文件 </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICC用户档案文件的路径和名称。 定义<span class="codeph"> <span class="varname"> destFile </span> </span>的像素类型和色彩空间。 如果<span class="codeph"> <span class="varname"> sourceFile </span> </span>具有嵌入式用户档案，或者如果<span class="codeph"> -imageprofile </span>也被指定，IC将转换为此用户档案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentEnterval  </span> </p> </td> 
   <td colname="col2"> <p>色彩空间转换的感知渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRel比色  </span> </p> </td> 
   <td colname="col2"> <p> 色彩空间转换的相对比色渲染方法（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbs比色  </span> </p> </td> 
   <td colname="col2"> <p>用于色彩空间转换的绝对比色渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>色彩空间转换的饱和度渲染方法。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>对某些颜色转换禁用黑点补偿 </p> <p>默认启动. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>转换颜色时禁用仿色（误差扩散）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainipixtype  </span> </p> </td> 
   <td colname="col2"> <p> 禁用从CMYK到RGB的自动转换。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>强制JPEG输入图像的解码和重新编码。 </p> <p> <b>注意：</b> 应用此选项可能会降低图像质量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>使用标准质量（双线性）重新取样滤镜。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>使用更高质量（Lanczos窗口）的重新取样滤镜（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>使用更高质量(FlashPix)的重新取样滤镜。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8双立方锐化  </span> </p> </td> 
   <td colname="col2"> <p>使用Photoshop风格8x8双立方锐化滤镜进行缩减像素采样。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> 如果指定为第一个选项，则在遇到无效选项时隐藏使用信息的输出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -覆盖 </span> </p> </td> 
   <td colname="col2"> <p>允许覆盖现有的<span class="codeph"> <span class="varname"> destFile </span> </span>。 默认情况下，会在文件名中附加一个数字后缀以防止覆盖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斯基菲登  </span> </p> </td> 
   <td colname="col2"> <p>忽略隐藏的源文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>发生错误时不停止处理。 仅在处理多个文件时有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>日志文件的路径和名称（默认为<span class="codeph"> stdout </span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>日志级别。 </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 -列表要处理的文件。</p>
   <p>1 —— 为不需要的文件添加报告。</p>
   <p>2 —— 添加进度报告。</p>
   <p>3 —— 为遇到的每个文件添加报告。</p>
   <p>4 —— 在文件级别添加进度报告。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>追加到日志文件（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>覆盖日志文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>日志级别2及更高版本的日志记录时间间隔（默认为3000）（毫秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>内存使用限制。 必须至少为10 MB。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent百 &lt;&gt; 分比 </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>内存使用限制。 默认为物理内存的25%。 如果<span class="codeph"> maxmem </span>和<span class="codeph"> maxmempercent </span>都未显式设置，则使用maxmempercent默认值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -版本 </span> </p> </td> 
   <td colname="col2"> <p> 返回此实用程序的版本信息。 不使用其他选项进行指定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支持的输入图像格式{#section-ab13d941d6724e65b9f84b62d949d31c}

下表列表了IC支持的图像文件格式和格式选项。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 格式</b> </p> </th> 
   <th class="entry"> <p> <b> 像素</b> <b> 类型位/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> 比特／陈</b> </p> </th> 
   <th class="entry"> <p> <b> 压缩</b> </p> </th> 
   <th class="entry"> <p> <b> 说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows位图） </p> </td> 
   <td> <p> RGB |已索引 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 未压缩 | RLE </p> </td> 
   <td> <p> 5/6位/渠道表示支持16位RGB(5-5-5和5-6-5位/渠道)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （封装的Postscript） </p> </td> 
   <td> <p> CMYK | RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 |二进制 | JPEG </p> </td> 
   <td> <p> 只支持Photoshop生成的EPS文件。 </p> </td> 
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
   <td> <p> 索引 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 如果存在，调色板中的透明度值将转换为alpha。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA |灰色 | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未压缩 |压缩 </p> </td> 
   <td> <p> 仅合并图像；图层和额外渠道将被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 仅位图数据；将忽略矢量数据。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 3 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 压缩的 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> 未压缩 | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 |包位 </p> </td> 
   <td> <p> 除了第一个关联的alpha渠道之外，还会忽略其他渠道。 </p> </td> 
  </tr> 
 </tbody> 
</table>

嵌入的ICC用户档案可在EPS、JPG、PSD、PNG和TIFF文件中识别。

嵌入路径和XMP元数据可在EPS、JPG、PSD和TIFF文件中识别。

## 示例 {#section-3c1986b30315431989bd76b1ee5bef6d}

以最佳质量转换单个图像，并将其保留在同一文件夹中：

`ic -convert src/myFile.png src/myFile.tif`

将&#x200B;*`srcFolder`*&#x200B;中的所有图像转换为JPEG编码的金字塔TIFF并放入&#x200B;*`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

转换&#x200B;*`srcFolder`*&#x200B;中的所有图像。 JPG文件的编码图像数据用于这些图像的其余图像金字塔的全分辨率级无损LZW压缩以及所有非JPG输入文件的整个输出图像。 像素类型、嵌入的颜色用户档案、XMP元数据等。 。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
