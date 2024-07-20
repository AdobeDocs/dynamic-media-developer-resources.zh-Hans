---
title: 嵌入式图像服务器请求
description: 图像服务器(IS)请求可用作材质图像。
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

图像服务器(IS)请求可用作材质图像。

按如下方式在`src=`命令中指定请求：

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`令牌区分大小写。

嵌套请求不得包含图像服务根路径（通常为 [!DNL http:// *[!DNL server]*/is/image/"]），但可能包含预处理规则令牌。

在嵌套请求中指定以下IS命令时（在请求URL中或在`catalog::Modifier`或`catalog::PostModifier`中），将忽略这些命令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

另外忽略的是应用于嵌入的IS请求的图像目录的`attribute::MaxPix`和`attribute::DefaultPix`。

如果嵌套请求的结果图像包含蒙版(alpha)数据，则始终会将该数据传递给材料。 使用纯色背景图像图层可避免不需要的Alpha。

通过包含`cache=on`，可以选择缓存嵌入式IS请求的图像结果。 默认情况下，将禁用中间数据的缓存。 仅当在合理的时间段内在不同的请求中重用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式进行缓存。
