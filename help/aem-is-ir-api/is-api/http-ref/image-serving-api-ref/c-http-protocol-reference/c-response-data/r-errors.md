---
description: 如果请求无法成功完成，则服务器将返回错误图像或HTTP响应状态（200以外），并同时返回错误消息。
solution: Experience Manager
title: 错误
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---

# 错误{#errors}

如果请求无法成功完成，则服务器将返回错误图像或HTTP响应状态（200以外），并同时返回错误消息。

响应状态值取决于错误的类型；对于最常见的错误，为“403”。 非图像请求类型的错误响应符合使用`req=`指定的格式。 （此时可能不会始终如一地实施。）

错误消息中包含的详细信息量可配置为`attribute::ErrorDetail`。

## 错误图像 {#section-92e9b20b2507433daa96923abc95f777}

可以将图像提供配置为返回呈现到图像中的错误消息。

有关详细信息，请参阅图像目录引用中的[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)。

如果成功生成错误图像，则HTTP响应状态为200。 如果处理错误图像时出错，则标准HTTP错误响应和文本消息将返回给客户端。

## 默认图像 {#section-66bf25fe6b434081bfae96d38d9be25e}

可以将“图像提供”配置为将缺失的图像替换为默认图像。 可以使用`attribute::DefaultImage`或`defaultImage=`命令指定默认图像。

## 另请参阅 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ,  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
