---
description: 无论sourceFile的类型如何，都可以应用以下选项。
solution: Experience Manager
title: 常用选项
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 常用选项{#common-options}

无论sourceFile的类型如何，都可以应用以下选项。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 字符串 </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置输出文件的文件夹(包括日志文件，如果 <span class="codeph"> -log </span> 指定)。 可以是绝对路径，也可以是相对于当前工作目录的绝对路径。 如果文件夹层次结构不存在，则会创建该文件夹层次结构。 不适用于通过 <span class="codeph"> -log </span>. 如果未指定，输出文件将写入其中 <span class="varname"> sourceFile </span> 中。 如果 <span class="varname"> destFile </span> ，则始终会将其写入到该位置，并且 <span class="codeph"> -destpath </span> 仅适用于次输出文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -图像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，则从晕影、从柜式样的合适面板图像或窗口覆盖样式的第一照明图像中提取（第一）视图图像。 提取的图像将另存为全分辨率TIFF文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>阻止生成目标文件。 从中快速提取属性非常有用 <span class="varname"> sourceFile </span>. 仅可选缩略图( <span class="codeph"> -thumbwidth </span>)，图像( <span class="codeph"> -image </span>)和日志文件( <span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>为输出文件中嵌入的RGB和灰度图像数据选择有损JPEG编码，而不是无损的PNG。 带有Alpha(RGBA)的图像始终使用PNG编码进行保存。 <span class="varname"> 伊瓦尔 </span> 指定JPEG质量(1...100);建议使用85或更高版本。 默认为 <span class="codeph"> -jpegquality 0 </span>，可选择PNG编码。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> 路径 </span> </span> </p> </td> 
  <td class="stentry"> <p>创建具有指定路径/名称的日志文件写入目标文件夹的所有输出文件的完整路径将写入日志文件，以及其他一些设置，如版本信息和遇到的任何警告或错误(请参阅 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 输出 </a> )。 如果 <span class="codeph"> -log </span> 未指定；在这种情况下，所有文本输出都将写入 <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 低优先级 <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>降低 <span class="filepath"> vntc </span> 进程。 可以使用此选项，以便 <span class="filepath"> vntc </span> 处理晕影时不会接管整个CPU。 它允许操作系统为其他更重要的流程提供更多时间。 <span class="varname"> 伊瓦尔 </span> 指定较低的优先级百分比(0.100)。 默认为 <span class="codeph">  — 低优先级0 </span>，不会降低 <span class="filepath"> vntc </span> 进程。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>指定 <span class="filepath"> vntc </span> 允许以字节为单位使用。 When <span class="filepath"> vntc </span> 达到最大内存限制，停止处理并产生错误。 <span class="varname"> 伊瓦尔 </span> 指定最大内存限制（以字节为单位）(0.. 3,758,096,384(3.5GB)。 When <span class="varname"> 伊瓦尔 </span> 为0，则最大内存限制会关闭。 默认为 <span class="codeph"> -maxmem 3221225472 </span>，表示最大内存限制为3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 分隔符" <span class="varname"> 字符串 </span>" </span> </p> </td> 
  <td class="stentry"> <p>为自动生成的输出文件名指定文件名和大小/分辨率后缀之间的分隔符。 如果未指定，则默认为“ — ”。 如果 <span class="varname"> destFile </span> 或 <span class="codeph"> -info </span> 指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 锐化 <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>可在处理期间锐化重新采样（缩放）的图像。 仅适用于文件柜样式文件的缩略图锐化。 </p> <p>指定0以禁用锐化（默认），指定1以启用正常锐化，指定2以仅启用亮度的USM锐化，指定3以启用每个颜色组件的USM锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>设置日志级别。 默认值为1，可输出所有信息、警告和错误消息。 设置为0可禁用除错误消息之外的所有消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 金额 </span> <span class="varname"> 半径 </span> <span class="varname"> 阈值 </span> </span> </p> </td> 
  <td class="stentry"> <p>设置USM锐化参数。 如果 <span class="codeph">  — 锐化 </span> 设置为0或1;必需 <span class="codeph">  — 锐化 </span> 设置为2或3。 <span class="varname"> 金额 </span> 是0.0..500.0范围内的实数值， <span class="varname"> 半径 </span> 是范围为0.0...10.0的实际值，和 <span class="varname"> 阈值 </span> 是介于0和255之间的整数。 请参阅 <span class="codeph"> op_usm= </span> ，以了解其他信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>验证给定的晕影是否是正确的生产晕影。 <span class="varname"> 伊瓦尔 </span> 表示晕影的最低文件版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> 伊瓦尔 </span> </span> </p> </td> 
  <td class="stentry"> <p>输出文件的文件版本。 如果已指定，则必须为0或有效的晕影文件版本（不大于默认文件版本）。 如果设置为0或未指定，则使用最新文件版本创建输出文件。 如果 <span class="codeph"> -info </span> 指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>返回此实用工具的版本信息。 指定不带文件名和其他选项。 </p> </td> 
 </tr> 
</table>
