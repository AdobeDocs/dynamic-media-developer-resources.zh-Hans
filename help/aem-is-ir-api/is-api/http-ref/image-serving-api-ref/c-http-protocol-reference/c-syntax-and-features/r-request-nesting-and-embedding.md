---
description: 图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。
seo-description: 图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。
seo-title: 请求嵌套和嵌入
solution: Experience Manager
title: 请求嵌套和嵌入
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 请求嵌套和嵌入{#request-nesting-and-embedding}

图像服务支持无限嵌套图像服务请求、嵌入图像渲染请求以及嵌入从外部服务器检索的图像。 只有图层图像和图层蒙版支持这些机制。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>某些电子邮件客户端和代理服务器可能会对用于嵌套和嵌入语法的花括号进行编码。 存在此问题的应用程序应使用括号而不是大括号。

## 嵌套图像服务请求 {#section-6954202119e0466f8ff27c79f4f039c8}

整个图像服务请求可以用作图层源，方法是使用以下语法在 `src=` (或 `mask=`)命令中指定它：

`…&src=is( nestedRequest)&…`

令 `is` 牌区分大小写。

嵌套请求不得包括服务器根路径(通常 ` http:// *[!DNL server]*/is/image/'`)。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>嵌套请求中的嵌套请求分隔符( `'(',')'`)和命令分隔符( `'?'`、 `'&'`、 `'='`)不得采用HTTP编码。 有效地，嵌套请求的编码必须与外部（嵌套）请求相同。

预处理规则应用于嵌套请求。

当在嵌套请求（在请求URL中或在或中）中指定时，将忽略 `catalog::Modifier` 以下命 `catalog::PostModifier`令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果嵌套请求的结果图像包括遮罩(alpha)数据，则它作为图层遮罩传递到嵌入层。

同时忽略应 `attribute::MaxPix`用于 `attribute::DefaultPix` 嵌套请求的图像目录和图像目录。

嵌套IS请求的图像结果可以通过包括来选择性地缓存 `cache=on`。 默认情况下，中间数据的缓存处于禁用状态。 仅当期望在合理的时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入式图像渲染请求 {#section-69c5548db930412b9b90d9b2951a6969}

在服务器上启用Scene7图像渲染后，渲染请求可以通过在src=（或mask=）命令中指定来用作图层源。 请使用以下语法：

` …&src=ir( *[!DNL renderRequest]*)&…`

令 `ir` 牌区分大小写。

*[!DNL renderRequest]* 是通常的图像渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>嵌套请求中的嵌套请求分隔符( `'(',')'`)和命令分隔符( `'?'`、 `'&'`、 `'='`)不得采用HTTP编码。 有效地，嵌入式请求的编码必须与外部（嵌入）请求相同。

在嵌套请求中指定以下图像渲染命令时，将忽略它们：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

同时忽略应 `attribute::MaxPix` 用于 `attribute::DefaultPix` 嵌套渲染请求的材料目录以及这些目录。

可以通过包括来选择性地缓存嵌套IR请求的图像结果 `cache=on`。 默认情况下，中间数据的缓存处于禁用状态。 仅当期望在合理的时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。

## 嵌入的FXG渲染请求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

在安装FXG图形渲染器(aka [!DNL AGMServer])并启用图像服务时，FXG请求可以在（或）命令中指定它们作为图层源 `src=` 使 `mask=`用。 请使用以下语法：

`…&src=fxg( renderRequest)&…`

令 `fxg` 牌区分大小写。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>FXG图形渲染仅在Scene7托管环境中可用，并且可能需要额外的许可。 有关详细信息，请与Scene7支持联系。

*[!DNL renderRequest]* 是通常的FXG渲染请求，不包括HTTP根路径 ` http:// *[!DNL server]*/agm/render/`。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>嵌套请求中的分隔 `'(',')'`符()和命令分隔符( `'?'`、 `'&'`、 `'='`)不能采用HTTP编码。 有效地，嵌入式请求的编码必须与外部（嵌入）请求相同。

在嵌套请求中指定以下FXG命令时，将忽略它们：

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

要为或命令指定外 `src=` 部URL, `mask=` 请用括号将外部URL或URL片段分隔开：

`…&src=( foreignUrl)&…`

重要信息嵌套请求中 `'(',')'`的分隔符()和命令分隔符( `'?'`、 `'&'`、 `'='`)不得采用HTTP编码。 有效地，嵌入式请求的编码必须与外部（嵌入）请求相同。

完全绝对URL(如 `attribute::AllowDirectUrls` 果已设置)，以及相对于的URL `attribute::RootUrl` 是允许的。 如果嵌入了绝对URL并且属性为：如 `AllowDirectUrls` 果为0，或者指定了相对URL且 `attribute::RootUrl` 为空。

虽然无法在请求URL的路径组件中直接指定外部URL，但可以设置一个预处理规则以允许将相对路径转换为绝对URL（请参阅以下示例）。

服务器根据HTTP响应中包含的缓存头对外部图像进行缓存。 如果既不存 `ETag` 在“上次修改时间”HTTP响应头，也不存在“上次修改时间”HTTP响应头，则不缓存该响应。 这可能导致对同一外来图像的重复访问性能不佳，因为图像服务需要在每次访问时重新获取和重新验证图像。

此机制支持图像转换(IC)实用程序支持的相同图像文件格式，但每个组件16位的源图像除外。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>图像服务将在首次使用外来图像时自动运行验证实用程序，以确保图像有效且在传输过程中未损坏。 这可能会导致首次访问稍有延迟。 为获得最佳性能，建议限制此类图像的大小和／或使用压缩良好的图像文件格式。

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

嵌套／嵌入式请求生成的图像的大小通常会自动优化。 如果启用了嵌套请求图像的缓存，可以通过指定嵌套图像的确切大小来实现增量性能增益，因此当重复使用缓存条目时不需要进一步缩放。

重要图像服务不支持嵌套或嵌入请求的多次编码。 嵌套和嵌入的请求必须像简单请求一样进行HTTP编码。

## 示例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**使用缓存分层模板：**

使用嵌套向图层模板添加缓存。 有限数量的背景图像被高度可变的文本覆盖。 初始模板字符串可能如下：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

稍作修改后，我们可以预缩放第0层图像并永久缓存它，从而减少服务器负载：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**嵌入Scene7图像渲染请求**

使用存储在以下位置的模板 [!DNL myCatalog/myTemplate];使用Scene7图像渲染为模板的第2层生成图像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

请注意嵌套的花括号。 图像渲染请求会嵌入对图像服务的回叫，以检索可重复的纹理。

## 另请参阅 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , mask= [，请求预处](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)理 [，图像渲染参考，模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，图像服务实 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[用程序](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
