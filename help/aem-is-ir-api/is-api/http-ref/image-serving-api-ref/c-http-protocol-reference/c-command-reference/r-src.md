---
description: 图层图像。
seo-description: 图层图像。
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

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
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>嵌套图像服务、图像渲染或外部请求。 </p> </td> 
 </tr> 
</table>

## 说明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定图像图层的源图像。

*`object`* 可以是目录条目或图像/SVG文件。

请参阅 [对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

嵌套或嵌入的请求用大括号括住。 在嵌入的图像服务请求前加 `is`上前缀，在嵌入的图像渲染请 `ir`求前加上前缀，在FXG图形渲染请求前加上前缀 `fxg`。 如果未指定前缀，则假定对外部服务器的请求。

请参阅 [请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

>[!NOTE]
>
>FXG图形渲染仅在Scene7托管环境中可用，并且可能需要额外的许可。 有关详细信息，请与Scene7支持联系。

## 属性 {#section-2c22bb89a35d470f833df8ba898efd93}

图层属性。 适用于 `layer=0` if `layer=comp`。 与同一层 `text=` 相互 `textPs=` 排斥，最后一次出现 `text=`、 `textPs=`或 `src=` 优先，并确定这是图像还是文本图层。 被效果图层忽略。

*`object`*不能解析到其中包含或命令的 `src=` 其 `mask=` 他目录记录 `catalog::Modifier`。 （使用请求嵌套实现类似效果。）

前 `is`缀、 `ir`前缀 `fxg` 和前缀区分大小写。

## 默认 {#section-a92f3882041b4d43ae2caf014647165f}

对于第0层，如果未指定，则使用URL路径组件中 `src=` 的对象。 其他图层没有默认值。

## 另请参阅 {#section-e467e03330564796932ac081f1c9c1d0}

[目录：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ，属性：:RootPath [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)Attribute::RootPath, [Text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),Ps [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[Text=mask=ObjectPath,ObjectTemplates, The Nesting and Embedding Requestsed](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
