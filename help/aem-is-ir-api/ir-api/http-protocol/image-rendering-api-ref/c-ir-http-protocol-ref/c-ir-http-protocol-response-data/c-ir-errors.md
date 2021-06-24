---
description: 如果请求无法成功完成，则服务器将返回错误图像或HTTP响应状态（200以外），并同时返回错误消息。
solution: Experience Manager
title: 错误
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 错误{#errors}

如果请求无法成功完成，则服务器将返回错误图像或HTTP响应状态（200以外），并同时返回错误消息。

响应状态值取决于错误的类型；对于最常见的错误，为“403”。 非图像请求类型的错误响应符合使用`req=`指定的格式。 （此时可能无法始终如一地实施。）

错误消息中包含的详细信息量可配置为`attribute::ErrorDetail`。

**错误图像**

可以将图像提供配置为返回呈现到图像中的错误消息。 有关详细信息，请参阅图像目录引用中的`attribute::ErrorImage` 。 如果成功生成错误图像，则HTTP响应状态为200。 如果处理错误图像时出错，则标准HTTP错误响应和文本消息将返回给客户端。

**另请参阅**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
