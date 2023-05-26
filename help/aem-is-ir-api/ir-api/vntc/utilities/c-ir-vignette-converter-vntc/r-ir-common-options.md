---
description: 不论sourceFile的类型如何，都可以应用以下选项。
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

不论sourceFile的类型如何，都可以应用以下选项。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 字符串 </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置输出文件的文件夹(包括日志文件，如果 <span class="codeph"> -log </span> 指定了)。 可以是绝对路径或相对于当前工作目录的相对路径。 如果文件夹层次结构不存在，则会创建该层次结构。 不适用于指定的文件 <span class="codeph"> -log </span>. 如果未指定，则输出文件将写入到 <span class="varname"> 源文件 </span> 位置。 如果 <span class="varname"> destFile </span> 指定时，将始终写入该位置，并且 <span class="codeph"> -destpath </span> 仅适用于辅助输出文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -图像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，则从晕影、从橱柜样式的合适面板图像或者窗口覆盖样式的第一照明图像提取（第一）视图图像。 提取的图像将另存为全分辨率TIFF文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>阻止生成目标文件。 可用于快速从提取属性 <span class="varname"> 源文件 </span>. 仅可选缩略图( <span class="codeph">  — 缩略图 </span>)，图像( <span class="codeph"> -image </span>)和日志文件( <span class="codeph"> -log </span>)生成。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>为嵌入到输出文件中的RGB和灰度图像数据选择有损JPEG编码，而不是无损PNG。 带有Alpha (RGBA)的图像始终使用PNG编码进行保存。 <span class="varname"> ival </span> 指定JPEG质量(1...100)；建议使用85或更高版本。 默认为 <span class="codeph"> -jpegquality 0 </span>，选择PNG编码。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> 路径 </span> </span> </p> </td> 
  <td class="stentry"> <p>使用指定的路径/名称创建日志文件写入目标文件夹的所有输出文件的完整路径以及某些其他设置（如版本信息和遇到的任何警告或错误）会写入日志文件(请参阅 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 输出 </a> 了解详细信息)。 如果符合以下条件，则不会创建日志文件 <span class="codeph"> -log </span> 未指定；在这种情况下，所有文本输出将写入 <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>降低 <span class="filepath"> vntc </span> 进程。 此函数可以用于 <span class="filepath"> vntc </span> 不会接管整个CPU来处理晕影。 它让操作系统有更多时间用于其他更重要的进程。 <span class="varname"> ival </span> 指定较低的优先级百分比(0..100)。 默认为 <span class="codeph"> -lowerpriority 0 </span>，不会降低的优先级 <span class="filepath"> vntc </span> 进程。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>指定最大内存量 <span class="filepath"> vntc </span> 允许以字节为单位。 时间 <span class="filepath"> vntc </span> 达到最大内存限制，它将停止处理并产生错误。 <span class="varname"> ival </span> 指定最大内存限制(以字节为单位，0.. 3,758,096,384 (3.5GB)。 时间 <span class="varname"> ival </span> 为0，将关闭最大内存限制。 默认为 <span class="codeph"> -maxmem 3221225472 </span>，这意味着最大内存限制为3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> 字符串 </span>” </span> </p> </td> 
  <td class="stentry"> <p>为自动生成的输出文件名指定置于文件名与大小/分辨率后缀之间的分隔符。 如果未指定，则默认为“ — ”。 忽略条件 <span class="varname"> destFile </span> 或 <span class="codeph"> -info </span> 已指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 锐化 <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>在处理期间启用重新取样（缩放）图像的锐化。 仅适用于压缩样式文件的缩略图锐化。 </p> <p>指定0可禁用锐化（默认值），指定1可启用普通锐化，指定2可仅针对亮度启用钝化蒙版，指定3可针对每个颜色组件启用钝化蒙版。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>设置日志级别。 默认值为1，这将输出所有信息性消息、警告消息和错误消息。 设置为0可禁用除错误消息之外的所有其他消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 数量 </span> <span class="varname"> 半径 </span> <span class="varname"> 阈值 </span> </span> </p> </td> 
  <td class="stentry"> <p>设置钝化蒙版参数。 忽略条件 <span class="codeph">  — 锐化 </span> 设置为0或1；在以下情况下需要 <span class="codeph">  — 锐化 </span> 设置为2或3。 <span class="varname"> 数量 </span> 是一个介于0.0...500.0之间的实值， <span class="varname"> 半径 </span> 是一个介于0.0...10.0之间的实值，并且 <span class="varname"> 阈值 </span> 是一个介于0和255之间的整数。 请参阅 <span class="codeph"> op_usm= </span> 有关更多信息，请参阅图像服务协议参考。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>验证给定的晕影是否为正确的生产晕影。 <span class="varname"> ival </span> 表示晕影的最小文件版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>输出文件的文件版本。 如果指定，则必须为0或有效的晕影文件版本（不得大于默认文件版本）。 如果设置为0或未指定，则使用最新文件版本创建输出文件。 忽略条件 <span class="codeph"> -info </span> 已指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 指定而不使用文件名和其他选项。 </p> </td> 
 </tr> 
</table>
