---
description: 映像验证实用程序。 此命令行实用程序验证图像文件以确保它们有效，并且图像服务可以轻松读取它们。
solution: Experience Manager
title: 确认
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# 确认{#validate}

映像验证实用程序。 此命令行实用程序验证图像文件以确保它们有效，并且图像服务可以轻松读取。

所有非PTIFF图像文件都必须通过验证，然后该文件才可供图像服务用作源图像。 PTIFF映像应在执行可能不可靠的复制操作后进行验证。

## 使用 {#usage}

` validate *`文件类型`* [ *`options`*] [ *`源文件`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 文件类型 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>源文件类型；必须至少指定一种（ — any允许IC支持的相同图像文件类型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令选项（见下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 源文件 </span> </span> </p> </td> 
  <td class="stentry"> <p> 图像文件。 全部或更多，用空格分隔。 </p> </td> 
 </tr> 
</table>

## 返回 {#section-67a7cf7c53144fbb8f24b818f4a10901}

如果成功，则为0。 如果发生错误，将返回非零值并将错误详细信息发送到 `stderr`.

## 选项 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含图像文件列表的单独文本文件。 每个文件一个记录。 如果 <span class="codeph"> -fileList </span> 包括， <span class="varname"> 源文件 </span> 不能指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>启用整个图像文件的验证。 默认情况下，仅验证图像标头。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>验证嵌入的颜色配置文件的有效性。 默认情况下，不选中正文配置文件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 拒绝每个图像组件为16位的图像。 在验证远程源映像时始终由映像服务器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 如果图像无效，则打印更多信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>禁用 <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> 输出。 仅返回状态。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>在文件验证失败时终止处理，即使尚未验证其他文件。 默认情况下，发生验证错误时将继续进行处理 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 指定而不使用其他选项。 </p> </td> 
 </tr> 
</table>
