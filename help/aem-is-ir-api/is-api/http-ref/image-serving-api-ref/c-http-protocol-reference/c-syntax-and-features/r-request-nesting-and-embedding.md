---
description: 图像服务支持对图像服务请求进行无限嵌套、嵌入图像渲染请求以及嵌入从外部服务器检索到的图像。 只有图层图像和图层蒙版支持这些机制。
solution: Experience Manager
title: 请求嵌套和嵌入
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# 请求嵌套和嵌入{#request-nesting-and-embedding}

图像服务支持对图像服务请求进行无限嵌套、嵌入图像渲染请求以及嵌入从外部服务器检索到的图像。 只有图层图像和图层蒙版支持这些机制。

>[!NOTE]
>
>某些电子邮件客户端和代理服务器可能会对用于嵌套和嵌入语法的大括号进行编码。 对于存在此问题的应用程序，应使用括号而不是大括号。

## 嵌套图像服务请求 {#section-6954202119e0466f8ff27c79f4f039c8}

通过使用以下语法在`src=`（或`mask=`）命令中指定整个图像服务请求，可以将其用作图层源：

`…&src=is( nestedRequest)&…`

`is`令牌区分大小写。

嵌套请求不得包含服务器根路径（通常为` http:// *[!DNL server]*/is/image/'`）。

>[!NOTE]
>
>嵌套请求分隔符字符(`'(',')'`)和嵌套请求中的命令分隔符字符(`'?'`、`'&'`、`'='`)不能进行HTTP编码。 实际上，嵌套请求的编码方式必须与外部（嵌套）请求相同。

预处理规则应用于嵌套请求。

在嵌套请求（在请求URL中或者在`catalog::Modifier`或`catalog::PostModifier`中）中指定时，将忽略以下命令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果嵌套请求的结果图像包括蒙版(alpha)数据，则将其作为图层蒙版传递到嵌入层。

另外忽略的是应用于嵌套请求的图像目录的`attribute::MaxPix`和`attribute::DefaultPix`。

通过包含`cache=on`，可以选择缓存嵌套IS请求的图像结果。 默认情况下，将禁用中间数据的缓存。 仅当预期中间图像应在合理时段内在不同的请求中重用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式进行缓存。

## 嵌入式图像渲染请求 {#section-69c5548db930412b9b90d9b2951a6969}

在服务器上启用Dynamic Media图像渲染后，可通过在src=（或mask=）命令中指定渲染请求来将其用作图层源。 使用以下语法：

` …&src=ir( *[!DNL renderRequest]*)&…`

`ir`令牌区分大小写。

*[!DNL renderRequest]*&#x200B;是常用的图像渲染请求，不包括HTTP根路径` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>嵌套请求分隔符字符(`'(',')'`)和嵌套请求中的命令分隔符字符(`'?'`、`'&'`、`'='`)不能进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定时，将忽略以下图像渲染命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

同样被忽略的是应用于嵌套渲染请求的材质目录的`attribute::MaxPix`和`attribute::DefaultPix`。

通过包含`cache=on`，可以选择缓存嵌套IR请求的图像结果。 默认情况下，将禁用中间数据的缓存。 仅当预期中间图像应在合理时段内在不同的请求中重用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式进行缓存。

## 嵌入的FXG渲染请求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

安装并启用带有图像服务的FXG图形渲染器（又称[!DNL AGMServer]）后，可通过在`src=`（或`mask=`）命令中指定FXG请求来将其用作图层源。 使用以下语法：

`…&src=fxg( renderRequest)&…`

`fxg`令牌区分大小写。

>[!NOTE]
>
>FXG图形渲染仅在Dynamic Media托管的环境中可用，并且可能需要额外的许可。 有关更多信息，请联系Dynamic Media技术支持。

*[!DNL renderRequest]*&#x200B;是常用的FXG渲染请求，不包括HTTP根路径` http:// *[!DNL server]*/agm/render/`。

>[!NOTE]
>
>嵌套请求中的分隔符字符(`'(',')'`)和命令分隔符字符(`'?'`、`'&'`、`'='`)不能进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定时，将忽略以下FXG命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外部图像源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

图像服务支持对外部HTTP服务器上的源图像的访问。

>[!NOTE]
>
>远程URL仅支持HTTP协议。

要为`src=`或`mask=`命令指定外部URL，请使用括号分隔外部URL或URL片段：

`…&src=( foreignUrl)&…`

重要信息：嵌套请求中的分隔符字符(`'(',')'`)和命令分隔符字符(`'?'`、`'&'`、`'='`)不能进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

允许使用完全绝对URL（如果已设置`attribute::AllowDirectUrls`）和相对`attribute::RootUrl`的URL。 如果嵌入了绝对URL并且属性： `AllowDirectUrls`为0，或者如果指定了相对URL并且`attribute::RootUrl`为空，则会发生错误。

虽然不能直接在请求URL的路径组件中指定外部URL，但可以设置预处理规则以允许将相对路径转换为绝对URL（请参阅下面的示例）。

服务器根据HTTP响应中包含的缓存标头来缓存外来图像。 如果`ETag`和Last-Modified HTTP响应标头都不存在，则不会缓存该响应。 这可能会导致对同一外来图像的重复访问性能降低，因为图像服务在每次访问时都需要重新获取和重新验证图像。

此机制支持与图像转换(IC)实用程序支持的图像文件格式相同的图像文件格式，但每个组件具有16位的源图像除外。

>[!NOTE]
>
>图像服务会在首次使用外来图像时自动运行验证实用程序，以确保图像有效并且在传输期间未损坏。 这可能会导致首次访问时稍微延迟。 为获得最佳性能，建议限制此类图像的大小和/或使用压缩得很好的图像文件格式。

## 限制 {#section-fb68e3f0d40947feb94d7bf183b64929}

嵌套/嵌入请求生成的图像大小通常会自动优化。 如果启用了嵌套请求图像的缓存，则可以通过指定嵌套图像的确切大小来实现性能增量提高，这样在重用缓存条目时就不需要进一步缩放。

重要信息图像服务不支持对嵌套或嵌入请求进行双重编码。 嵌套和嵌入的请求必须像简单请求一样进行HTTP编码。

## 示例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**缓存的分层模板：**

使用嵌套将缓存添加到分层模板。 有限数量的背景图像由高度可变的文本覆盖。 初始模板字符串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

稍作修改，我们就可以预先缩放第0层图像并持久地对其进行缓存，从而减少服务器负载：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Dynamic Media图像渲染的嵌入请求**

使用存储在[!DNL myCatalog/myTemplate]中的模板；使用Dynamic Media图像渲染为模板的layer2生成图像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

请注意嵌套的大括号。 图像渲染请求将回调嵌入到图像服务，以检索可重复的纹理。

## 另请参阅 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)，[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，[请求预处理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，图像渲染引用，[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)，[图像服务实用程序](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
