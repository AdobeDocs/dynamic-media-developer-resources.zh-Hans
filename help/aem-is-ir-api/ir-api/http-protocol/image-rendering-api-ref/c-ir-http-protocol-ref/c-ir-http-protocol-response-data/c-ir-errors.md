---
title: 错误
description: 如果请求无法成功完成，则服务器会返回一个错误图像或200以外的HTTP响应状态并返回一条错误消息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# 错误{#errors}

如果请求无法成功完成，则服务器会返回一个错误图像或200以外的HTTP响应状态并返回一条错误消息。

响应状态值取决于错误的类型；对于大多数常见错误，值为“403”。 非图像请求类型的错误响应符合指定的格式 `req=`. （当前可能未得到一致实施。）

错误消息中包含的详细信息量可通过进行配置 `attribute::ErrorDetail`.

**错误图像**

图像服务可以配置为返回渲染到图像中的错误消息。 参见 `attribute::ErrorImage` 详细信息，请参阅图像目录引用。 如果成功生成错误图像，则HTTP响应状态为200。 如果在处理错误图像时出错，则将标准HTTP错误响应和文本消息返回到客户端。

**另请参阅**

[attribute：：ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ， [attribute：：ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
