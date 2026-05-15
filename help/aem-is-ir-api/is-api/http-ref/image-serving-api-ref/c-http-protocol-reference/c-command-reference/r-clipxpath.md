---
title: clipXPath
description: 反转图层剪辑路径。 指定当前图层的排除剪辑路径。 图层中由clipXPath=定义的区域内的任何部分都呈现为透明。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
TQID: 'https://experienceleague.adobe.com/G8pumLDbSj2TX80gqSTw-Bu4HxlRn92gyFpETIImBWw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# clipXPath{#clipxpath}

反转图层剪辑路径。 指定当前图层的排除剪辑路径。 图层中由clipXPath=定义的区域内的任何部分都呈现为透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>嵌入到图层源图像中的路径的名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

请参阅[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以获取其他信息，包括`*`pathName`*`和`*`pathDefinition`*`的说明。

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 如果未指定`clipPath=`，则忽略。 被效果层忽略。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

无。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
