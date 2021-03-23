---
description: 如果请求无法成功完成，服务器将返回错误图像或200以外的HTTP响应状态，并返回错误消息。
seo-description: 如果请求无法成功完成，服务器将返回错误图像或200以外的HTTP响应状态，并返回错误消息。
seo-title: 错误
solution: Experience Manager
title: 错误
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 2%

---


# 错误{#errors}

如果请求无法成功完成，服务器将返回错误图像或200以外的HTTP响应状态，并返回错误消息。

响应状态值取决于错误的类型；对于大多数常见错误，它为“403”。 非图像请求类型的错误响应符合使用`req=`指定的格式。 （此时可能不能一致实现。）

包含在错误消息中的详细信息量可配置为`attribute::ErrorDetail`。

**错误图像**

可以将图像服务配置为返回呈现到图像中的错误消息。 有关详细信息，请参阅图像目录参考中的`attribute::ErrorImage`。 如果成功生成错误图像，则HTTP响应状态为200。 如果处理错误图像时发生错误，则标准HTTP错误响应和文本消息将返回给客户端。

**另请参阅**

[attribute:::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
