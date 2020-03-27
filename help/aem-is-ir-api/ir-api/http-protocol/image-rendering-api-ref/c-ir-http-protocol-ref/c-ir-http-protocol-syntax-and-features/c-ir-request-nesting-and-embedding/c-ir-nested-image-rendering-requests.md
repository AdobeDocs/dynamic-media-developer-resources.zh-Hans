---
description: 对于高级应用程序，可以像从图像服务获得的图像一样，将渲染操作的结果用作物质图像。
seo-description: 对于高级应用程序，可以像从图像服务获得的图像一样，将渲染操作的结果用作物质图像。
seo-title: 嵌套的图像渲染请求
solution: Experience Manager
title: 嵌套的图像渲染请求
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 嵌套的图像渲染请求{#nested-image-rendering-requests}

对于高级应用程序，可以像从图像服务获得的图像一样，将渲染操作的结果用作物质图像。

渲染请求可以通过在命令中指定来用作材料图像，如 `src=` 下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

令 `ir` 牌区分大小写。

嵌套请求不得包括图像渲染根路径(通常 `http:// *[!DNL server]*/ir/render/'`)，但可能包括预处理规则令牌。

当在嵌套请求（在请求URL中或在或中）中指定时，将忽略 `catalog::Modifier` 以下命 `catalog::PostModifier`令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

同时忽略应 `attribute::MaxPix` 用于 `attribute::DefaultPix` 嵌套渲染请求的材料目录以及这些目录。

可以通过包括来选择性地缓存嵌套IR请求的图像结果 `cache=on`。 默认情况下，中间数据的缓存处于禁用状态。 仅当期望在合理的时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
