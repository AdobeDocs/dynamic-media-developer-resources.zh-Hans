---
description: 倒层剪辑路径。 为当前图层指定排除剪辑路径。 图层中clipXPath=定义的区域内的任何部分都呈现为透明。
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# clipXPath{#clipxpath}

倒层剪辑路径。 为当前图层指定排除剪辑路径。 图层中clipXPath=定义的区域内的任何部分都呈现为透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>层源图像中嵌入的路径的名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

有关其他信息，请参阅[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)，包括`*`pathName`*`和`*`pathDefinition`*`的说明。

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

层属性。 应用于当前层或复合图像（如果`layer=comp`）。 如果未指定`clipPath=`，则忽略。 被效果层忽略。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

无。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
