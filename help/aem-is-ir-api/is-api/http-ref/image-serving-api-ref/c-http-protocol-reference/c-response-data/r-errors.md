---
description: 如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。
seo-description: 如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。
seo-title: 错误
solution: Experience Manager
title: 错误
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a08f3f5a-3013-4d35-9612-25190a4c99fa
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 2%

---


# 错误{#errors}

如果请求无法成功完成，服务器将返回错误图像或除200之外的HTTP响应状态，并返回错误消息。

响应状态值取决于错误的类型；对于大多数常见错误，它为“403”。 非映像请求类型的错误响应符合使用`req=`指定的格式。 （此时可能不会一致实施。）

错误消息中包含的详细信息量可配置为`attribute::ErrorDetail`。

## 错误图像{#section-92e9b20b2507433daa96923abc95f777}

可以将图像服务配置为返回呈现到图像中的错误消息。

有关详细信息，请参阅图像目录参考中的[属性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)。

如果错误图像生成成功，则HTTP响应状态为200。 如果处理错误图像时出错，则标准HTTP错误响应和文本消息将返回给客户端。

## 默认图像{#section-66bf25fe6b434081bfae96d38d9be25e}

可以将图像服务配置为用默认图像替换缺少的图像。 可以使用`attribute::DefaultImage`或`defaultImage=`命令指定默认图像。

## 另请参阅 {#section-e261d7f224ca4546bb64bf8cb909db08}

[属性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ，属 [性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)，属 [性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
