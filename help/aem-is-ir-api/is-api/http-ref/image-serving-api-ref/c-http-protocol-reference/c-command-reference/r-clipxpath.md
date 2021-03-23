---
description: 反转图层剪辑路径。 指定当前图层的排除剪辑路径。 图层中clipXPath=定义的区域内的任何部分都呈现为透明。
seo-description: 反转图层剪辑路径。 指定当前图层的排除剪辑路径。 图层中clipXPath=定义的区域内的任何部分都呈现为透明。
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# clipXPath{#clipxpath}

反转图层剪辑路径。 指定当前图层的排除剪辑路径。 图层中clipXPath=定义的区域内的任何部分都呈现为透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>嵌入在图层源图像中的路径名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

请参见[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以了解其他信息，包括`*`pathName`*`和`*`pathDefinition`*`的说明。

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 如果未指定`clipPath=`，则忽略。 被效果图层忽略。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

无。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
