---
description: 图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们是有效的，并且图像服务可以毫不费力地读取这些文件。
seo-description: 图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们是有效的，并且图像服务可以毫不费力地读取这些文件。
seo-title: 确认
solution: Experience Manager
title: 确认
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 确认{#validate}

图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们是有效的，并且图像服务可以毫不费力地读取这些文件。

所有非PTIFF图像文件必须通过验证，才能使图像服务作为源图像可用。 在复制操作可能不可靠后，应验证PTIFF图像。

## 使用 {#usage}

` validate *`fileType`* [ *``*] [ *`、sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg| -ptif| -any </span> </p> <p>源文件类型；必须至少指定一种（-any允许IC支持的相同图像文件类型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 选项 </span></span> </p> </td> 
  <td class="stentry"> <p>其他命令选项（请参阅下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 源 <span class="varname"> 文件 </span></span> </p> </td> 
  <td class="stentry"> <p> 图像文件。 无或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

如果成功，则为0。 如果发生错误，则返回非零值，并向发送错误详细信息 `stderr`。

## 选项 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span></span> </p> </td> 
  <td class="stentry"> <p>指定包含图像文件列表的单独文本文件。 每个文件记录一条。 如 <span class="codeph"> 果包含 </span> -fileList，则 <span class="varname"> 不 </span> 能指定sourceFile。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>支持验证整个图像文件。 默认情况下，仅验证图像标题。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>验证嵌入的颜色用户档案的有效性。 默认情况下，用户档案主体不被选中。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 拒绝每个图像组件16位的图像。 在验证远程源图像时始终由图像服务器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 如果图像无效，则打印更多信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>禁用 <span class="codeph"> stdout </span>/ <span class="codeph"> stderr输 </span> 出。 只返回状态。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>在文件验证失败时终止处理，即使其他文件尚未验证。 默认情况下，当发生验证错误时，处理将继续 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 不使用其他选项进行指定。 </p> </td> 
 </tr> 
</table>

