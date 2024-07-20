---
title: opac
description: 调整图像不透明度。 允许降低图像、文本、纯色或效果图层的前景不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# opac{#opac}

调整图像不透明度。 允许降低图像、文本、纯色或效果图层的前景不透明度。

`opac= *`不透明度`*[, *`填充不透明度`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">不透明度</span> </p> </td> 
  <td class="stentry"> <p>主不透明度(0...100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">填充不透明度</span> </p></td> 
  <td class="stentry"> <p>填充不透明度(0...100 int)。 </p></td> 
 </tr> 
</table>

图像图层的前景不透明度由图像的图层蒙版或Alpha通道决定，如果两者都不存在，则是100%。 文本图层的前景不透明度为100%，纯色图层的前景不透明度由`color=`设置。

`opac=`从不修改用`color=`或`bgColor=`填充的区域的不透明度，纯色和效果图层的前景区域除外（使用`color=`设置）。

当在图像、文本或纯色图层中指定时，*`opacity`*&#x200B;应用整个图层，包括所有关联的效果图层，而&#x200B;*`fillOpacity`*&#x200B;仅应用于主要图层内容。 在效果层中指定时，*`opacity`*&#x200B;将应用于效果层，而&#x200B;*`fillOpacity`*&#x200B;将被忽略。

主层内容的有效不透明度为(*`opacity`* &#42; *`fillOpacity`* / 100)。 效果层的有效不透明度为（主&#x200B;*`opacity`* &#42;效果&#x200B;*`opacity`* / 100）。

## 属性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

层属性。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，表示图层不透明度没有变化。

## 示例 {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

本例中的文本不透明度为90&#42;70/100=63%，效果图层不透明度为90&#42;50/100=45%。

## 另请参阅 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
