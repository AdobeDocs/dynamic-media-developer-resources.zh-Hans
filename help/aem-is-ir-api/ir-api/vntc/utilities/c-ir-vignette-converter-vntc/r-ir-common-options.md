---
description: 无论sourceFile的类型如何，都可以应用以下选项。
seo-description: 无论sourceFile的类型如何，都可以应用以下选项。
seo-title: 常用选项
solution: Experience Manager
title: 常用选项
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 常用选项{#common-options}

无论sourceFile的类型如何，都可以应用以下选项。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath字 <span class="varname"> 符串 </span></span> </p> </td> 
  <td class="stentry"> <p>要在其中放置输出文件的文件夹(如果指定了-log，则包 <span class="codeph"> 括日志 </span> 文件)。 可以是绝对路径或相对于当前工作目录的相对路径。 如果文件夹层次结构不存在，则将创建它。 不适用于使用-log指定的 <span class="codeph"> 文件 </span>。 如果未指定，则输出文件将写入源文件所在 <span class="varname"> 的文 </span> 件夹中。 如果 <span class="varname"> 指 </span> 定destFile，则始终将其写入该位置，并且 <span class="codeph"> -destpath仅应 </span> 用于辅助输出文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -图像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，则从暗角、从柜式样的合适的面板图像或窗口覆盖样式的第一照明图像中提取（第一）视图图像。 提取的图像将保存为全分辨率TIFF文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>防止生成目标文件。 对于从sourceFile快速提取属性 <span class="varname"> 很有用 </span>。 只生成可选缩略图( <span class="codeph"> -thumbwidth </span>)、图像( <span class="codeph"> -image </span>)和日志文件( <span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>为嵌入在输出文件中的RGB和灰度图像数据选择有损JPEG编码，而不是无损PNG。 始终使用PNG编码保存带有alpha(RGBA)的图像。 <span class="varname"> ival </span> 指定JPEG质量(1...100);建议使用85或更高版本。 默认值为 <span class="codeph"> -jpegquality 0 </span>，它将选择PNG编码。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span></span> </p> </td> 
  <td class="stentry"> <p>创建具有指定路径／名称的日志文件写入目标文件夹的所有输出文件的完整路径将写入日志文件，以及一些其他设置，如版本信息和遇到的任何警告或错误(有关详细信息，请参阅 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 输 </a> 出)。 如果未指定-log，则 <span class="codeph"> 不会创 </span> 建日志文件；在这种情况下，所有文本输出都将写入 <span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>降低vntc过程的 <span class="filepath"> 优 </span> 先级。 这样，vntc在处理暗角 <span class="filepath"> 时 </span> 不会接管整个CPU。 它允许操作系统为其他更重要的进程提供更多时间。 <span class="varname"> ival指 </span> 定较低的优先级百分比(0..100)。 默认值 <span class="codeph"> 为-lowerpriority 0 </span>，这不会降低vntc进程的 <span class="filepath"> 优先级 </span> 。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>指定允许vntc使用的最 <span class="filepath"> 大内 </span> 存量（以字节为单位）。 当vntc <span class="filepath"> 达 </span> 到最大内存限制时，它停止处理并产生错误。 <span class="varname"> ival指 </span> 定最大内存限制（以字节为单位）(0.. 3,758,096,384(3.5 GB)。 当 <span class="varname"> 值 </span> 为0时，最大内存限制关闭。 默认为 <span class="codeph"> -maxmem 3221225472 </span>，这意味着最大内存限制为3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>为自动生成的输出文件名指定位于文件名和大小／分辨率后缀之间的分隔符。 如果未指定，则默认为“-”。 如果指定 <span class="varname"> destFile </span> 或 <span class="codeph"> -info，则 </span> 忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -锐化 <span class="varname"> 间隔 </span></span> </p> </td> 
  <td class="stentry"> <p>支持在处理过程中对图像进行重新取样（缩放）的锐化。 仅适用于文件柜样式文件的缩览图锐化。 </p> <p>指定0可禁用锐化（默认），指定1可启用正常锐化，指定2可仅启用亮度的USM锐化，指定3可为每个颜色组件启用USM锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>设置日志级别。 默认值为1，它输出所有信息性、警告和错误消息。 设置为0可禁用除错误消息之外的所有消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm数量 <span class="varname"> 半径 </span> 阈值 <span class="varname"> - </span><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>设置USM锐化参数。 如果- <span class="codeph"> sharpen设 </span> 置为0或1，则忽略；如果- <span class="codeph"> sharpen设置为2 </span> 或3，则为必需。 <span class="varname"> amount </span> 是0.0...500.0范围内的实数值， <span class="varname"> radius </span> 是0.0....0范围内的实数值， <span class="varname"> threshold </span> 是0到255之间的整数。 有关其他信息，请参 <span class="codeph"> 阅图像服务协 </span> 议参考中op_usm=的说明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>验证给定暗角是否是正确的生产暗角。 <span class="varname"> ival表 </span> 示暗角的最低文件版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>输出文件的文件版本。 如果指定，则必须为0或有效的暗角文件版本（不大于默认文件版本）。 如果设置为0或未指定，则使用最新文件版本创建输出文件。 如果指定 <span class="codeph"> 了-info, </span> 则忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 指定时不带文件名和其他选项。 </p> </td> 
 </tr> 
</table>

