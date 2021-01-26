---
description: 如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。
seo-description: 如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。
seo-title: 错误
solution: Experience Manager
title: 错误
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# 错误{#errors}

如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。

响应状态值取决于错误的类型；对于大多数常见错误，它为“403”。 非映像请求类型的错误响应符合使用`req=`指定的格式。 （此时可能未实现一致。）

错误消息中包含的详细信息量可配置为`attribute::ErrorDetail`。

**错误图像**

可以将图像服务配置为返回呈现到图像中的错误消息。 有关详细信息，请参阅图像目录参考中的`attribute::ErrorImage`。 如果错误图像生成成功，则HTTP响应状态为200。 如果处理错误图像时出错，则标准HTTP错误响应和文本消息将返回给客户端。

**另请参阅**

[属性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [属性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
