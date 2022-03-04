---
title: 嵌套图像渲染请求
description: 对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像提供中获得的图像一样。
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

对于高级应用，可以将渲染操作的结果用作材料图像，就像从图像提供中获得的图像一样。

通过在 `src=` 命令：

` …&src=ir{ *[!DNL renderRequest]*}&…`

的 `ir` 令牌区分大小写。

嵌套请求不得包含图像渲染根路径(通常为 `http:// *[!DNL server]*/ir/render/'`)，但可能包含预处理规则令牌。

在嵌套请求中(在请求URL中或在 `catalog::Modifier` 或 `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

也会被忽略 `attribute::MaxPix` 和 `attribute::DefaultPix` 应用于嵌套渲染请求的材料目录的子目录。

可选择通过包括 `cache=on`. 默认情况下，中间数据的缓存处于禁用状态。 仅当中间图像在合理时间段内在其他请求中重复使用时，才应启用缓存。 标准服务器端缓存管理适用。 数据以无损格式缓存。
