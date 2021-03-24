---
description: 对于高级应用，可以将渲染操作的结果用作物质图像，就像从图像服务获得的图像一样。
solution: Experience Manager
title: 嵌套图像渲染请求
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# 嵌套图像渲染请求{#nested-image-rendering-requests}

对于高级应用，可以将渲染操作的结果用作物质图像，就像从图像服务获得的图像一样。

通过在`src=`命令中指定渲染请求，可以将其用作物质图像，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`令牌区分大小写。

嵌套请求不得包含图像渲染根路径（通常为`http:// *[!DNL server]*/ir/render/'`），但可能包含预处理规则令牌。

在嵌套请求（在请求url中或在`catalog::Modifier`或`catalog::PostModifier`中）中指定时，将忽略以下命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

同样被忽略的是应用于嵌套渲染请求的材料目录的`attribute::MaxPix`和`attribute::DefaultPix`。

可以通过包括`cache=on`来选择性地缓存嵌套IR请求的图像结果。 默认情况下，中间数据的缓存处于禁用状态。 仅当预期在合理时间段内在不同请求中重复使用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
