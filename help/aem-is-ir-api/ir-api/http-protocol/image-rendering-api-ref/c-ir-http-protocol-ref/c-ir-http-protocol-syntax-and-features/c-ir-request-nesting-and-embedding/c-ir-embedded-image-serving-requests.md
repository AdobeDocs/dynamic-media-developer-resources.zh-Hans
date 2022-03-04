---
title: 嵌入式图像服务器请求
description: 图像服务器(IS)请求可用作物质图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 嵌入式图像服务器请求{#embedded-image-server-requests}

图像服务器(IS)请求可用作物质图像。

在 `src=` 命令：

` …&src=is( *[!DNL imageServingRequest]*)&…`

的 `is` 令牌区分大小写。

嵌套请求不得包含图像服务根路径(通常 [!DNL http:// *[!DNL server]*/is/image/"])，但可能包含预处理规则令牌。

在嵌套请求(在请求URL中或在 `catalog::Modifier` 或 `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

也会被忽略 `attribute::MaxPix` 和 `attribute::DefaultPix` 应用于嵌入式IS请求的图像目录的URL。

如果嵌套请求的结果图像包含掩码(Alpha)数据，则始终将其传递到材料。 使用纯色背景图像层以避免不需要的Alpha。

可选择通过包括 `cache=on`. 默认情况下，中间数据的缓存处于禁用状态。 仅当中间图像在合理时间段内在其他请求中重复使用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
