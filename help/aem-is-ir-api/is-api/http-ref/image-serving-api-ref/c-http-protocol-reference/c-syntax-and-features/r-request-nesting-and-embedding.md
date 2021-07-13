---
description: 图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求，以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。
solution: Experience Manager
title: 请求嵌套和嵌入
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# 请求嵌套和嵌入{#request-nesting-and-embedding}

图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求，以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。

>[!NOTE]
>
>某些电子邮件客户端和代理服务器可能会对用于嵌套和嵌入语法的大括号进行编码。 对于这个问题的应用程序，应使用圆括号而不是大括号。

## 嵌套图像服务请求 {#section-6954202119e0466f8ff27c79f4f039c8}

通过在`src=`（或`mask=`）命令中使用以下语法指定整个图像服务请求，可以将其用作层源：

`…&src=is( nestedRequest)&…`

`is`令牌区分大小写。

嵌套请求不得包含服务器根路径（通常为` http:// *[!DNL server]*/is/image/'`）。

>[!NOTE]
>
>嵌套请求中的嵌套请求分隔符字符(`'(',')'`)和命令分隔符字符(`'?'`、`'&'`、`'='`)不得进行HTTP编码。 实际上，嵌套请求的编码必须与外部（嵌套）请求的编码相同。

预处理规则将应用于嵌套请求。

在嵌套请求中（在请求URL中、在`catalog::Modifier`或`catalog::PostModifier`中）指定时，将忽略以下命令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果嵌套请求的结果图像包含掩码(Alpha)数据，则它将作为图层掩码传递给嵌入层。

此外，还忽略了应用于嵌套请求的图像目录的`attribute::MaxPix`和`attribute::DefaultPix`。

可以选择通过包含`cache=on`来缓存嵌套IS请求的图像结果。 默认情况下，中间数据的缓存处于禁用状态。 仅当中间图像预期在合理时间段内在其他请求中重复使用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入式图像渲染请求 {#section-69c5548db930412b9b90d9b2951a6969}

在服务器上启用“Dynamic Media图像渲染”后，渲染请求可以用作层源，方法是在src=（或mask=）命令中指定这些请求。 使用以下语法：

` …&src=ir( *[!DNL renderRequest]*)&…`

`ir`令牌区分大小写。

*[!DNL renderRequest]* 是常规的图像渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>嵌套请求中的嵌套请求分隔符字符(`'(',')'`)和命令分隔符字符(`'?'`、`'&'`、`'='`)不得进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定以下图像渲染命令时，将忽略该命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

此外，还忽略了应用于嵌套呈现请求的材料目录的`attribute::MaxPix`和`attribute::DefaultPix`。

可选择通过包含`cache=on`来缓存嵌套IR请求的图像结果。 默认情况下，中间数据的缓存处于禁用状态。 仅当中间图像预期在合理时间段内在其他请求中重复使用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入式FXG渲染请求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

在安装并启用“图像服务”的FXG图形渲染器（即[!DNL AGMServer]）后，可以通过在`src=`（或`mask=`）命令中指定FXG请求作为层源。 使用以下语法：

`…&src=fxg( renderRequest)&…`

`fxg`令牌区分大小写。

>[!NOTE]
>
>FXG图形渲染仅在Dynamic Media托管环境中可用，并且可能需要额外的许可。 请联系Dynamic Media技术支持以了解更多信息。

*[!DNL renderRequest]* 是常规的FXG渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/agm/render/`。

>[!NOTE]
>
>嵌套请求中的分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

在嵌套请求中指定以下FXG命令时，将忽略该命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外国图像源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

图像服务支持访问外部HTTP服务器上的源图像。

>[!NOTE]
>
>远程URL仅支持HTTP协议。

要为`src=`或`mask=`命令指定外部URL，请用圆括号分隔外部URL或URL片段：

`…&src=( foreignUrl)&…`

重要信息嵌套请求中的分隔符(`'(',')'`)和命令分隔符(`'?'`、`'&'`、`'='`)不得进行HTTP编码。 实际上，嵌入请求的编码必须与外部（嵌入）请求的编码相同。

完全绝对URL（如果设置了`attribute::AllowDirectUrls`），并允许相对于`attribute::RootUrl`的URL。 如果嵌入了绝对URL和属性，则会发生错误：`AllowDirectUrls`为0，或者如果指定了相对URL且`attribute::RootUrl`为空。

虽然不能直接在请求URL的路径组件中指定外部URL，但可以设置一个预处理规则以允许将相对路径转换为绝对URL（请参阅以下示例）。

服务器会根据HTTP响应中包含的缓存标头来缓存外来图像。 如果`ETag`和上次修改时间的HTTP响应标头都不存在，则不会缓存响应。 这可能会导致对同一外国图像重复访问时性能不佳，因为图像服务需要在每次访问时重新获取并重新验证图像。

此机制支持与图像转换(IC)实用程序支持的图像文件格式相同，但源图像每个组件具有16位除外。

>[!NOTE]
>
>当首次使用外部映像时，图像服务将自动运行验证实用程序，以确保映像有效且在传输过程中未损坏。 这可能会导致首次访问出现轻微延迟。 为获得最佳性能，建议限制此类图像的大小和/或使用能够很好地压缩的图像文件格式。

## 限制 {#section-fb68e3f0d40947feb94d7bf183b64929}

通常，会自动优化嵌套/嵌入请求生成的图像大小。 如果启用了嵌套请求图像的缓存，则可通过指定嵌套图像的确切大小来实现增量性能提升，因此当缓存条目被重用时，无需进一步缩放。

重要信息图像服务不支持对嵌套或嵌入的请求进行双重编码。 嵌套请求和嵌入请求必须像简单请求一样进行HTTP编码。

## 示例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**分层模板并缓存：**

使用嵌套向分层模板添加缓存。 有限数量的背景图像会被高度可变的文本覆盖。 初始模板字符串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

通过稍作修改，我们可以预缩放第0层映像并持久缓存它，从而减少服务器负载：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**嵌入Dynamic Media图像渲染请求**

使用存储在[!DNL myCatalog/myTemplate]中的模板；使用Dynamic Media图像渲染为模板的layer2生成图像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

请注意嵌套的大括号。 图像渲染请求嵌入对图像服务的回调，以检索可重复的纹理。

## 另请参阅 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，请求预处理 [，图像渲染引用， ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)模板 [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) [图像服务实用程序](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
