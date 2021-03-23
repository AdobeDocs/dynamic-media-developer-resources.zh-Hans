---
description: 图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。
seo-description: 图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。
seo-title: 请求嵌套和嵌入
solution: Experience Manager
title: 请求嵌套和嵌入
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# 请求嵌套和嵌入{#request-nesting-and-embedding}

图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。

>[!NOTE]
>
>某些电子邮件客户端和代理服务器可能会对用于嵌套和嵌入语法的花括号进行编码。 存在此问题的应用程序应使用括号而不是花括号。

## 嵌套图像服务请求{#section-6954202119e0466f8ff27c79f4f039c8}

整个图像服务请求可以用作图层源，方法是使用以下语法在`src=`（或`mask=`）命令中指定它：

`…&src=is( nestedRequest)&…`

`is`令牌区分大小写。

嵌套请求不得包含服务器根路径（通常为` http:// *[!DNL server]*/is/image/'`）。

>[!NOTE]
>
>嵌套请求中的嵌套请求分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得采用HTTP编码。 有效地，嵌套请求的编码必须与外部（嵌套）请求相同。

预处理规则应用于嵌套请求。

在嵌套请求（在请求URL中或在`catalog::Modifier`或`catalog::PostModifier`中）中指定时，将忽略以下命令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果嵌套请求的结果图像包含蒙版(Alpha)数据，则将其作为图层蒙版传递给嵌入图层。

同样被忽略的图像目录的`attribute::MaxPix`和`attribute::DefaultPix`适用于嵌套请求。

可以通过包含`cache=on`对嵌套IS请求的图像结果进行缓存。 默认情况下，中间数据的缓存处于禁用状态。 仅当预期在合理时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入式图像渲染请求{#section-69c5548db930412b9b90d9b2951a6969}

在服务器上启用Dynamic Media图像渲染后，渲染请求可通过在src=（或mask=）命令中指定来用作图层源。 使用以下语法：

` …&src=ir( *[!DNL renderRequest]*)&…`

`ir`令牌区分大小写。

*[!DNL renderRequest]* 是通常的图像渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>嵌套请求中的嵌套请求分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得采用HTTP编码。 有效地，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定时，将忽略以下图像渲染命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

同样被忽略的是应用于嵌套渲染请求的材料目录的`attribute::MaxPix`和`attribute::DefaultPix`。

可以通过包括`cache=on`来选择性地缓存嵌套IR请求的图像结果。 默认情况下，中间数据的缓存处于禁用状态。 仅当预期在合理时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入的FXG渲染请求{#section-c817e4b4f7da414ea5a51252ca7e120a}

在安装FXG图形渲染器(aka [!DNL AGMServer])并启用图像服务时，可以在`src=`（或`mask=`）命令中指定FXG请求作为图层源。 使用以下语法：

`…&src=fxg( renderRequest)&…`

`fxg`令牌区分大小写。

>[!NOTE]
>
>FXG图形渲染仅在Dynamic Media托管环境中可用，并且可能需要其他许可。 有关详细信息，请与Dynamic Media技术支持联系。

*[!DNL renderRequest]* 是通常的FXG渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/agm/render/`。

>[!NOTE]
>
>嵌套请求中的分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得采用HTTP编码。 有效地，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定时，将忽略以下FXG命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外部图像源{#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

图像服务支持访问外部HTTP服务器上的源图像。

>[!NOTE]
>
>远程URL仅支持HTTP协议。

要为`src=`或`mask=`命令指定外来URL，请用括号分隔外来URL或URL片段：

`…&src=( foreignUrl)&…`

重要信息：嵌套请求中的分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得采用HTTP编码。 有效地，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

完整绝对URL（如果设置了`attribute::AllowDirectUrls`），并允许相对于`attribute::RootUrl`的URL。 如果嵌入了绝对URL并且包含以下属性，则会发生错误：`AllowDirectUrls`为0，或者如果指定了相对URL且`attribute::RootUrl`为空。

虽然无法在请求URL的路径组件中直接指定外部URL，但可以设置预处理规则以允许将相对路径转换为绝对URL（请参阅以下示例）。

服务器根据HTTP响应中包含的缓存头对外部图像进行缓存。 如果`ETag`和上次修改时间的HTTP响应头都不存在，则不缓存响应。 这可能会导致同一外来图像的重复访问性能较差，因为图像服务需要在每次访问时重新提取和重新验证图像。

此机制支持图像转换(IC)实用程序支持的相同图像文件格式，但每个组件包含16位的源图像除外。

>[!NOTE]
>
>图像服务将在首次使用外来图像时自动运行验证实用程序，以确保图像有效且在传输过程中未损坏。 这可能会导致第一次访问稍有延迟。 为获得最佳性能，建议限制此类图像的大小和/或使用压缩良好的图像文件格式。

## 限制{#section-fb68e3f0d40947feb94d7bf183b64929}

通常，嵌套/嵌入请求生成的图像大小会自动优化。 如果启用嵌套请求图像的缓存，可以通过指定嵌套图像的确切大小来实现增量性能增益，因此当重用缓存条目时不需要进一步缩放。

重要信息：图像服务不支持嵌套或嵌入请求的多次编码。 嵌套和嵌入的请求必须像简单请求一样进行HTTP编码。

## 示例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**使用缓存分层模板：**

使用嵌套将缓存添加到分层模板。 有限数量的背景图像会覆盖高度可变的文本。 初始模板字符串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

只需稍作修改，我们就可以预缩放0层图像并永久缓存它，从而减少服务器负载：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**嵌入Dynamic Media图像渲染请求**

使用存储在[!DNL myCatalog/myTemplate]中的模板；使用Dynamic Media图像渲染为模板的layer2生成图像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

请注意嵌套的花括号。 “图像渲染”请求嵌入对图像服务的回叫，以检索可重复的纹理。

## 另请参阅 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , mask= [，请求预](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)处理，图像渲染参考 [，模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3),图像服 [务实用程序](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) [, ](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
