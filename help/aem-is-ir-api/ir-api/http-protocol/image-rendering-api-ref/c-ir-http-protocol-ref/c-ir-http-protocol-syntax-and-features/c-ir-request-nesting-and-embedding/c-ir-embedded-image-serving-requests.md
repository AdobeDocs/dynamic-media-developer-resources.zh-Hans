---
description: 图像服务器(IS)请求可用作物质图像。
solution: Experience Manager
title: 嵌入式图像服务器请求
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# 嵌入式图像服务器请求{#embedded-image-server-requests}

图像服务器(IS)请求可用作物质图像。

在`src=`命令中指定请求，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

`is`令牌区分大小写。

嵌套请求不得包含图像服务根路径(通常为[!DNL http:// *[!DNL server]*/is/image/&quot;])，但可能包含预处理规则令牌。

在嵌套请求（在请求URL中或在`catalog::Modifier`或`catalog::PostModifier`中）中指定时，将忽略以下IS命令：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

同样被忽略的图像目录的`attribute::MaxPix`和`attribute::DefaultPix`适用于嵌入式IS请求。

如果嵌套请求的结果图像包含蒙版(Alpha)数据，则始终将其传递给材料。 使用纯色背景图像图层以避免不需要的Alpha。

可以通过包含`cache=on`对嵌入式IS请求的图像结果进行缓存。 默认情况下，中间数据的缓存处于禁用状态。 仅当预期在合理时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
