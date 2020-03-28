---
description: 图像服务器(IS)请求可用作物质图像。
seo-description: 图像服务器(IS)请求可用作物质图像。
seo-title: 嵌入式图像服务器请求
solution: Experience Manager
title: 嵌入式图像服务器请求
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 嵌入式图像服务器请求{#embedded-image-server-requests}

图像服务器(IS)请求可用作物质图像。

在命令中指定请 `src=` 求，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

令 `is` 牌区分大小写。

嵌套请求不得包括图像服务根路径(通常为[!DNL http:// *[!DNL server]*/is/image/&quot;])，但可能包括预处理规则令牌。

当在嵌套请求（在请求URL中或在或中）中指定时，将忽略以 `catalog::Modifier` 下IS命 `catalog::PostModifier`令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

同时忽略应 `attribute::MaxPix` 用于 `attribute::DefaultPix` 嵌入式IS请求的图像目录和图像目录。

如果嵌套请求的结果图像包括遮罩(alpha)数据，则始终将其传递给材料。 使用纯色背景图像图层以避免不需要的alpha。

嵌入式IS请求的图像结果可以通过包括来选择性地缓存 `cache=on`。 默认情况下，中间数据的缓存处于禁用状态。 仅当期望在合理的时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
