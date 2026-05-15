---
description: 映像验证实用程序。 此命令行实用程序验证图像文件以确保它们有效，并且图像服务可以轻松读取它们。
solution: Experience Manager
title: 驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
TQID: 'https://experienceleague.adobe.com/gWtVDo3ounZMncdhwLMJsoRaPyZP3E1Fi98L8fX6XFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 1%

---

# 驗證{#validate}

映像验证实用程序。 此命令行实用程序验证图像文件以确保它们有效，并且图像服务可以轻松读取。

所有非PTIFF图像文件都必须通过验证，然后该文件才可供图像服务用作源图像。 PTIFF映像应在执行可能不可靠的复制操作后进行验证。

## 使用 {#usage}

` validate *`fileType`* [ *`选项`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | — 任意</span> </p> <p>Source文件类型；必须至少指定一种（ — any允许IC支持的相同图像文件类型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">选项</span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令选项（见下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> 图像文件。 全部或更多，用空格分隔。 </p> </td> 
 </tr> 
</table>

## 返回 {#section-67a7cf7c53144fbb8f24b818f4a10901}

如果成功，则为0。 如果发生错误，则返回非零值，并将错误详细信息发送到`stderr`。

## 選項 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含图像文件列表的单独文本文件。 每个文件一个记录。 如果包括<span class="codeph"> -fileList </span>，则不能指定<span class="varname"> sourceFile </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 读取像素</span> </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> — 详细</span> </p> </td> 
  <td class="stentry"> <p> 如果图像无效，则打印更多信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 静音</span> </p> </td> 
  <td class="stentry"> <p>禁用<span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>输出。 仅返回状态。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>在文件验证失败时终止处理，即使尚未验证其他文件。 默认情况下，发生验证错误时将继续进行处理 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 版本</span> </p> </td> 
  <td class="stentry"> <p>返回此实用程序的版本信息。 指定而不使用其他选项。 </p> </td> 
 </tr> 
</table>
