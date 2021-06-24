---
description: 对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像提供中获得的图像一样。
solution: Experience Manager
title: 嵌套图像渲染请求
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 嵌套图像渲染请求{#nested-image-rendering-requests}

对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像提供中获得的图像一样。

呈现请求可通过在`src=`命令中指定来用作物质图像，如下所示：

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

此外，还忽略了应用于嵌套呈现请求的材料目录的`attribute::MaxPix`和`attribute::DefaultPix`。

可选择通过包含`cache=on`来缓存嵌套IR请求的图像结果。 默认情况下，中间数据的缓存处于禁用状态。 仅当中间图像预期在合理时间段内在其他请求中重复使用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
