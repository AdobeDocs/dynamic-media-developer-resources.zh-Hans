---
title: src
description: 图层图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# src{#src}

图层图像。

` src= *`对象`*|{[is|ir|fxg]'{' *`嵌套请求`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>图像对象。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 嵌套请求 </span> </p> </td> 
  <td class="stentry"> <p>嵌套图像服务、图像渲染或外部请求。 </p> </td> 
 </tr> 
</table>

## 说明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定图像图层的源图像。

*`object`* 可以是目录条目或图像/SVG文件。

请参阅 [对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

嵌套或嵌入的请求由大括号括起来。 为嵌入的图像服务请求添加前缀 `is`，嵌入的图像渲染请求 `ir`、和包含的FXG图形渲染请求 `fxg`. 如果未指定前缀，则假定对外服务器的请求为。

请参阅 [请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## 属性 {#section-2c22bb89a35d470f833df8ba898efd93}

层属性。 应用于 `layer=0` 如果 `layer=comp`. 与互斥 `text=` 和 `textPs=` 在同一层中；最后一次出现的 `text=`， `textPs=`，或 `src=` 优先并确定这是图像图层还是文本图层。 被效果层忽略。

*`object`*不能解析为其他包含 `src=` 或 `mask=` 命令在其中 `catalog::Modifier`. （使用请求嵌套可实现类似效果。）

此 `is`， `ir`、和 `fxg` 前缀区分大小写。

## 默认 {#section-a92f3882041b4d43ae2caf014647165f}

对于第0层，使用URL的路径组件中的对象，如果 `src=` 未指定。 其他图层没有默认值。

## 另请参阅 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog：：Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ， [属性：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)， [文本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)， [蒙版=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)， [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
