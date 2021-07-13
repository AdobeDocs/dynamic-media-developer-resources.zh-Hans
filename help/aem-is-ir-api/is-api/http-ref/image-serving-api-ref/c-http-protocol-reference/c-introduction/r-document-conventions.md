---
description: 本文档使用以下约定。
solution: Experience Manager
title: 文档约定
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: e93de3fa-dde1-4d79-93aa-9ad800840cfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 文档约定{#document-conventions}

本文档使用以下约定。

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>文本 </p> </td> 
  <td class="stentry"> <p>在语法部分中，非斜体文本是文字。 此规则不适用于空格和符号[ ] { } | *。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>在描述性部分中，单引号中的非斜体文本为文字。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 参数 </span> </p> </td> 
  <td class="stentry"> <p>斜体表示要用实际值替换的变量或参数。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 命令=  </span> </p> </td> 
  <td class="stentry"> <p>尾随为“=”的名称是指图像提供HTTP协议命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 属性：:Item  </span> </p> </td> 
  <td class="stentry"> <p>带有<span class="codeph">属性前缀的名称：</span>是指图像目录属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目录：:Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为<span class="codeph">目录的名称：</span>是指图像目录数据字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>前缀为<span class="codeph"> icc的名称：</span>是指ICC颜色配置文件映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 字体：：项目  </span> </p> </td> 
  <td class="stentry"> <p>前缀为<span class="codeph">字体的名称：</span>是指字体映射中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 宏：项目  </span> </p> </td> 
  <td class="stentry"> <p>带有<span class="codeph">宏前缀的名称：</span>是指宏定义表中的字段。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 规则集：：项目  </span> </p> </td> 
  <td class="stentry"> <p>前缀为<span class="codeph">规则集的名称：</span>是指URL预处理规则集中的元素。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 默认：:Item  </span> </p> </td> 
  <td class="stentry"> <p>默认名称前缀为<span class="codeph">:</span>是指默认图像目录的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [可 <span class="varname"> 选 </span>]  </span> </p> </td> 
  <td class="stentry"> <p>可选语法元素用方括号括起来。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[可 <span class="varname"> 选 </span>]  </span> </p> </td> 
  <td class="stentry"> <p><span class="varname">可选</span>语法元素可以重复一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 项目1  </span>|  <span class="varname"> item2  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直条表示可以使用左侧的单个语法项目或右侧的项目。 必须只选择一个项目。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> 组 </span>}  </span> </p> </td> 
  <td class="stentry"> <p>大括号用于对语法元素进行分组。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> 组 </span>}  </span> </p> </td> 
  <td class="stentry"> <p>组中的语法元素可以重复一次或多次。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP请求中不允许有空格（空格或制表符）。 本文档有时仅为清晰起见，在语法元素之间使用空格。 </p> </td> 
 </tr> 
</table>
