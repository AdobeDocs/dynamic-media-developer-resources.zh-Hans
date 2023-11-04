---
description: 如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。
solution: Experience Manager
title: 错误
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# 错误{#errors}

如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。

响应状态值取决于错误类型；对于大多数常见错误，值为“403”。 非图像请求类型的错误响应符合指定的格式 `req=`. （当前可能无法始终如一地执行。）

错误消息中包含的详细信息量可通过进行配置 `attribute::ErrorDetail`.

## 错误图像 {#section-92e9b20b2507433daa96923abc95f777}

图像服务可以配置为返回渲染到图像中的错误消息。

请参阅 [attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) 详细信息，请参阅图像目录引用。

如果成功生成错误图像，则HTTP响应状态为200。 如果在处理错误图像时出错，则将标准HTTP错误响应和文本消息返回到客户端。

## 默认图像 {#section-66bf25fe6b434081bfae96d38d9be25e}

图像服务可以配置为用默认图像替换缺少的图像。 可以使用以下任一方式指定默认图像 `attribute::DefaultImage` 或 `defaultImage=` 命令。

## 另请参阅 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute：：ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ， [attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)， [attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)， [默认图像=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
