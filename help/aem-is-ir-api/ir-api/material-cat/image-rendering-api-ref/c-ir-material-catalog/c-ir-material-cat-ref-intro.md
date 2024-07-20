---
description: 本文档介绍了Dynamic Media图像渲染的材质目录。
solution: Experience Manager
title: 简介
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# 简介{#introduction}

本文档介绍了Dynamic Media图像渲染的材质目录。

**目标受众**

本文档面向经验丰富的程序员和网站开发人员，他们想要将Dynamic Media图像渲染用于网站或自定义应用程序。

假定读者熟悉Dynamic Media图像创作和图像渲染、一般HTTP协议标准和惯例以及基本的成像术语。

**文档惯例**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>文本 </p> </td> 
  <td class="stentry"> <p>在语法部分中，非斜体文本为文本；这不适用于空格和符号[ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'文本' </p> </td> 
  <td class="stentry"> <p>在描述性部分中，单引号中的非斜体文本是文字的。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">参数</span> </p> </td> 
  <td class="stentry"> <p>斜体表示要用实际值替换的变量或参数。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">属性：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“attribute：：”为前缀的名称是指图像目录属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph">目录：：项目</span> </td> 
  <td class="stentry"> <p>带有“catalog：：”前缀的名称是指材料目录数据字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“icc：：”为前缀的名称是指ICC颜色配置文件映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">宏：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“macro：：”为前缀的名称是指宏定义表中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">规则集：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“ruleset：：”为前缀的名称是指URL预处理规则集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">默认值：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“default：：”为前缀的名称是指默认图像目录的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">晕影：：项目</span> </p> </td> 
  <td class="stentry"> <p>以“晕影：：”为前缀的名称是指晕影映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname">可选</span> ] </p> </td> 
  <td class="stentry"> <p>可选语法元素用方括号括起来。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname">可选</span> ] </p> </td> 
  <td class="stentry"> <p>可选的语法元素可以不重复或多次重复。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">项1 </span>| <span class="varname">项2 </span> </p> </td> 
  <td class="stentry"> <p>垂直条表示可以使用左侧的单个语法项或右侧的项。 只能选择一个项目。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname">组</span> } </p> </td> 
  <td class="stentry"> <p>大括号用于对语法元素进行分组。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname">组</span> } </p> </td> 
  <td class="stentry"> <p>组中的语法元素可以重复一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空格。 </p> </td> 
  <td class="stentry"> <p>HTTP请求中不允许使用空格（空格或制表符）。 本文档偶尔会在语法元素之间使用空格，以仅供参考。 </p> </td> 
 </tr> 
</table>
