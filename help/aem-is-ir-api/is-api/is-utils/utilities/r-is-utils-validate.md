---
description: 图像验证实用程序。 此命令行实用程序会验证图像文件以确保它们有效，并且图像服务可以无困难地读取它们。
solution: Experience Manager
title: 确认
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 确认{#validate}

图像验证实用程序。 此命令行实用程序会验证图像文件以确保它们有效，并且图像服务可以无困难地读取它们。

所有非PTIFF图像文件都必须通过验证，然后才能将该文件提供给图像作为源图像。 在执行可能不可靠的复制操作后，应验证PTIFF图像。

## 使用 {#usage}

` validate *``* [ *``*] [ *`fileTypestionssourceFile`* [ … ]]`

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
  <td class="stentry"> <p> 图像文件。 无或多个，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 返回结果 {#section-67a7cf7c53144fbb8f24b818f4a10901}

0（如果成功）。 如果发生错误，则返回非零值，并将错误详细信息发送到`stderr`。

## 选项 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含图像文件列表的单独文本文件。 每个文件记录一条。 如果包含<span class="codeph"> -fileList </span>，则不能指定<span class="varname"> sourceFile </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>启用整个图像文件的验证。 默认情况下，仅验证图像标头。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>验证嵌入的颜色配置文件的有效性。 默认情况下，不会选中配置文件主体。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 拒绝每个图像组件具有16位的图像。 验证远程源图像时始终由图像服务器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 如果图像无效，则打印更多信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>禁用<span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>输出。 仅返回状态。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>在发生文件验证失败时终止处理，即使尚未验证其他文件也是如此。 默认情况下，当发生验证错误时，处理会继续 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>返回此实用工具的版本信息。 指定而不使用其他选项。 </p> </td> 
 </tr> 
</table>
