---
description: 如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。
solution: Experience Manager
title: 错误
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
TQID: 'https://experienceleague.adobe.com/qqe0JDlFGu08lAe-K3Ww9AtefwQInwBzZswiXsvqryo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 1%

---

# 错误{#errors}

如果请求无法成功完成，则服务器会返回错误图像或200以外的HTTP响应状态以及错误消息。

响应状态值取决于错误类型；对于大多数常见错误，值为“403”。 非图像请求类型的错误响应符合`req=`中指定的格式。 （当前可能无法始终如一地执行。）

错误消息中包含的详细信息数量可使用`attribute::ErrorDetail`进行配置。

## 错误图像 {#section-92e9b20b2507433daa96923abc95f777}

图像服务可以配置为返回渲染到图像中的错误消息。

有关详细信息，请参阅图像目录引用中的[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)。

如果成功生成错误图像，则HTTP响应状态为200。 如果在处理错误图像时出错，则将标准HTTP错误响应和文本消息返回到客户端。

## 默认图像 {#section-66bf25fe6b434081bfae96d38d9be25e}

图像服务可以配置为用默认图像替换缺少的图像。 可以使用`attribute::DefaultImage`或`defaultImage=`命令指定默认图像。

## 另请参阅 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute：：ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ，[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)，[attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)，[defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
