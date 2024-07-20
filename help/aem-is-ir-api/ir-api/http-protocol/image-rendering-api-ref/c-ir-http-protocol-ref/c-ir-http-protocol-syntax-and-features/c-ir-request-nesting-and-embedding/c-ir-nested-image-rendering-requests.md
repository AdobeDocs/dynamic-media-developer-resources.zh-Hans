---
title: 嵌套图像渲染请求
description: 对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像服务获得的图像一样。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 嵌套图像渲染请求{#nested-image-rendering-requests}

对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像服务获得的图像一样。

通过在`src=`命令中指定渲染请求，可以将渲染请求用作材质图像，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

`ir`令牌区分大小写。

嵌套请求不得包含图像渲染根路径（通常为`http:// *[!DNL server]*/ir/render/'`），但可能包含预处理规则令牌。

在嵌套请求中指定以下命令时（在请求URL中或在`catalog::Modifier`或`catalog::PostModifier`中），将忽略这些命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

同样被忽略的是应用于嵌套渲染请求的材质目录的`attribute::MaxPix`和`attribute::DefaultPix`。

通过包含`cache=on`，可以选择缓存嵌套IR请求的图像结果。 默认情况下，将禁用中间数据的缓存。 仅当在合理的时间段内在不同的请求中重用中间图像时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式进行缓存。
