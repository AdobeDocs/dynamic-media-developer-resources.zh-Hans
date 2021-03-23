---
description: 图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们有效，并且图像服务可以毫不费力地读取。
seo-description: 图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们有效，并且图像服务可以毫不费力地读取。
seo-title: 确认
solution: Experience Manager
title: 确认
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---


# 确认{#validate}

图像验证实用程序。 此命令行实用程序会验证图像文件，以确保它们有效，并且图像服务可以毫不费力地读取。

所有非PTIFF图像文件都必须通过验证，然后才能使图像服务作为源图像可用。 PTIFF图像应在可能不可靠的复制操作后进行验证。

## 使用 {#usage}

` validate *`fileTyperopets `* [ *``*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>源文件类型；必须至少指定一种（ — any允许IC支持的相同图像文件类型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 选项  </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令选项（请参阅下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 图像文件。 无或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 返回{#section-67a7cf7c53144fbb8f24b818f4a10901}

0（如果成功）。 如果发生错误，则返回非零值，并将错误详细信息发送到`stderr`。

## 选项 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含图像文件列表的单独文本文件。 每个文件一条记录。 如果包含<span class="codeph"> -fileList </span>，则不能指定<span class="varname"> sourceFile </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>启用整个图像文件的验证。 默认情况下，仅验证图像标头。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>验证嵌入的颜色用户档案的有效性。 默认情况下，不检查用户档案正文。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 拒绝每个图像组件16位的图像。 验证远程源图像时始终由图像服务器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 如果图像无效，则打印详细信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>禁用<span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>输出。 只返回状态。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>在发生文件验证失败时终止处理，即使尚未验证其他文件也是如此。 默认情况下，当发生验证错误时，处理将继续 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 指定时没有其他选项。 </p> </td> 
 </tr> 
</table>

