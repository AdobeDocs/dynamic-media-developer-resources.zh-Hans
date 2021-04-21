---
description: 图层图像。
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# src{#src}

图层图像。

` src= *`objectnestedRequest`*|{[is|ir|fxg]'{' *``*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>图像对象。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>嵌套图像服务、图像渲染或外部请求。 </p> </td> 
 </tr> 
</table>

## 说明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定图像图层的源图像。

*`object`* 可以是目录条目或图像/SVG文件。

请参阅[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

嵌套或嵌入的请求用大括号括起。 在嵌入的图像服务请求前加上`is`前缀，在嵌入的图像渲染请求中加上`ir`前缀，在FXG图形渲染请求中加上`fxg`前缀。 如果未指定前缀，则假定对外部服务器的请求。

请参阅[请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

## 属性 {#section-2c22bb89a35d470f833df8ba898efd93}

图层属性。 适用于`layer=comp`时的`layer=0`。 与同一层中的`text=`和`textPs=`互斥；最后一次出现`text=`、`textPs=`或`src=`的情况将优先，并确定这是图像还是文本图层。 被效果图层忽略。

*`object`*可能无法解析到其`catalog::Modifier`中包含`src=`或`mask=`命令的其他目录记录。 （使用请求嵌套实现类似效果。）

`is`、`ir`和`fxg`前缀区分大小写。

## 默认 {#section-a92f3882041b4d43ae2caf014647165f}

对于第0层，如果未指定`src=`，则使用URL路径组件中的对象。 没有其他图层的默认值。

## 另请参阅 {#section-e467e03330564796932ac081f1c9c1d0}

[目录：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ，属 [性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),PsPs [=文本，掩码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) [=，对象，模板，模板模板，请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
