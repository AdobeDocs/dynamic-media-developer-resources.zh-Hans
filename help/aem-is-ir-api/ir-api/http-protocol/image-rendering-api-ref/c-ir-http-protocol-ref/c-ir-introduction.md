---
description: 本文档描述了Dynamic Media图像渲染的HTTP协议。
solution: Experience Manager
title: 简介
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# 简介{#introduction}

本文档描述了Dynamic Media图像渲染的HTTP协议。

只描述了协议的公开可用方面。 服务器可支持保留供Dynamic Media客户端软件使用的其他命令。

**预期受众**

本文档面向希望将Dynamic Media图像渲染用于网站或自定义应用程序的有经验的程序员和网站开发人员。

假定读者熟悉Dynamic Media图像创作和图像渲染、一般HTTP协议标准和惯例以及基本的图像术语。

**文档惯例**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>文本 </p> </td> 
  <td class="stentry"> <p>在语法部分，非斜体文本为文字；这不适用于空白和符号[ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>在描述性章节中，单引号中的非斜体文本为文字。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 参数 </span> </p> </td> 
  <td class="stentry"> <p>斜体表示要用实际值替换的变量或参数。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 属性：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“attribute::”的名称指图像目录属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“catalog::”的名称是指材料目录数据字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“icc::”的名称指ICC颜色用户档案映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 宏：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“macro::”的名称指宏定义表中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 规则集：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“ruleset::”的名称指URL预处理规则集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 默认值：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为“default::”的名称指默认图像目录的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> 暗角：:Item  </span> </td> 
  <td class="stentry"> <p>前缀为“暗角：:”的名称指暗角映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">可选</span> ] </p> </td> 
  <td class="stentry"> <p>可选的语法元素用方括号括起来。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">可选</span> ] </p> </td> 
  <td class="stentry"> <p>可选语法元素可重复无或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> item2  </span> </p> </td> 
  <td class="stentry"> <p>垂直条指示可以使用左侧的单个语法项或右侧的项。 必须只选择一个项目。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>大括号用于对语法元素进行分组。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> 群組 </span> } </p> </td> 
  <td class="stentry"> <p>组中的语法元素可重复一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP请求中不允许使用空格（空格或制表符）。 此文档偶尔会在语法元素之间使用空白，以仅用于清晰性。 </p> </td> 
 </tr> 
</table>

**常用术语**

** *`MSS`* **材料规范段：请求中两个选择命令之间的一组材料属性。

** *`vignette`* **在Dynamic Media图像创作中准备的用于图像渲染的图像。
