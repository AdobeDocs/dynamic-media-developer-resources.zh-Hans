---
description: 无论sourceFile的类型如何，都可以应用以下选项。
solution: Experience Manager
title: 常用选项
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 常用选项{#common-options}

无论sourceFile的类型如何，都可以应用以下选项。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath字 <span class="varname"> 符串  </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置输出文件的文件夹（包括日志文件，如果指定了<span class="codeph"> -log </span>）。 可以是绝对路径，也可以是相对于当前工作目录的绝对路径。 如果文件夹层次结构不存在，则会创建该文件夹层次结构。 不适用于使用<span class="codeph"> -log </span>指定的文件。 如果未指定，则输出文件将写入<span class="varname"> sourceFile </span>所在的文件夹中。 如果指定了<span class="varname"> destFile </span>，则始终会将其写入到该位置，并且<span class="codeph"> -destpath </span>仅适用于次输出文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -图像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，则从晕影、从柜式样的合适面板图像或窗口覆盖样式的第一照明图像中提取（第一）视图图像。 提取的图像将另存为全分辨率TIFF文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>阻止生成目标文件。 对于快速从<span class="varname"> sourceFile </span>提取属性非常有用。 只生成可选的缩略图(<span class="codeph"> -thumbwidth </span>)、图像(<span class="codeph"> -image </span>)和日志文件(<span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>为输出文件中嵌入的RGB和灰度图像数据选择有损JPEG编码，而不是无损PNG。 带有Alpha(RGBA)的图像始终使用PNG编码进行保存。 <span class="varname"> ival </span> 指定JPEG质量(1...100);建议使用85或更高版本。默认值为<span class="codeph"> -jpegquality 0 </span>，这将选择PNG编码。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 日志路 <span class="varname"> 径  </span> </span> </p> </td> 
  <td class="stentry"> <p>创建具有指定路径/名称的日志文件写入目标文件夹的所有输出文件的完整路径将写入日志文件，以及其他一些设置，如版本信息和遇到的任何警告或错误（有关详细信息，请参阅<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">输出</a>）。 如果未指定<span class="codeph"> -log </span>，则不会创建日志文件；在这种情况下，所有文本输出都将写入<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 低优先级 <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>降低<span class="filepath"> vntc </span>进程的优先级。 可以使用此选项，以便<span class="filepath"> vntc </span>在处理晕影时不会接管整个CPU。 它允许操作系统为其他更重要的流程提供更多时间。 <span class="varname"> ival </span> 指定较低的优先级百分比(0.100)。默认值为<span class="codeph"> -lowerpriority 0 </span>，它不会降低<span class="filepath"> vntc </span>进程的优先级。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定允许<span class="filepath"> vntc </span>使用的最大内存量（以字节为单位）。 当<span class="filepath"> vntc </span>达到最大内存限制时，它会停止处理并产生错误。 <span class="varname"> ival </span> 指定最大内存限制（以字节为单位）(0..3,758,096,384(3.5GB)。 当<span class="varname"> ival </span>为0时，最大内存限制将关闭。 默认值为<span class="codeph"> -maxmem 3221225472 </span>，这表示最大内存限制为3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>为自动生成的输出文件名指定文件名和大小/分辨率后缀之间的分隔符。 如果未指定，则默认为“ — ”。 如果指定了<span class="varname"> destFile </span>或<span class="codeph"> -info </span>，则忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 锐化日 <span class="varname"> 期  </span> </span> </p> </td> 
  <td class="stentry"> <p>可在处理期间锐化重新采样（缩放）的图像。 仅适用于文件柜样式文件的缩略图锐化。 </p> <p>指定0以禁用锐化（默认），指定1以启用正常锐化，指定2以仅启用亮度的USM锐化，指定3以启用每个颜色组件的USM锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>设置日志级别。 默认值为1，可输出所有信息、警告和错误消息。 设置为0可禁用除错误消息之外的所有消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm量 <span class="varname"> 半径 </span> <span class="varname"> 阈 </span> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>设置USM锐化参数。 如果将<span class="codeph"> -sharpen </span>设置为0或1，则忽略此问题；如果将<span class="codeph"> -sharpen </span>设置为2或3，则此参数为必需参数。 <span class="varname"> amount </span> 是范围0.0..500.0中的实数值，  <span class="varname"> radius </span> 是范围0.0..10.0中的实数值， <span class="varname"> 阈 </span> 值是0到255之间的整数。有关其他信息，请参阅图像服务协议参考中<span class="codeph"> op_usm= </span>的说明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>验证给定的晕影是否是正确的生产晕影。 <span class="varname"> ival </span> 表示晕影的最低文件版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 版本 <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>输出文件的文件版本。 如果已指定，则必须为0或有效的晕影文件版本（不大于默认文件版本）。 如果设置为0或未指定，则使用最新文件版本创建输出文件。 如果指定了<span class="codeph"> -info </span>，则忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>返回此实用工具的版本信息。 指定不带文件名和其他选项。 </p> </td> 
 </tr> 
</table>
