---
title: 错误
description: 如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 错误{#errors}

如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。

响应状态值取决于错误类型；对于大多数常见错误，值为“403”。 非图像请求类型的错误响应符合`req=`中指定的格式。 （当前可能未得到一致实施。）

错误消息中包含的详细信息数量可使用`attribute::ErrorDetail`进行配置。

**错误图像**

图像服务可以配置为返回渲染到图像中的错误消息。 有关详细信息，请参阅图像目录引用中的`attribute::ErrorImage`。 如果成功生成错误图像，则HTTP响应状态为200。 如果在处理错误图像时出错，则将标准HTTP错误响应和文本消息返回到客户端。

**另请参阅**

[attribute：：ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ， [attribute：：ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
