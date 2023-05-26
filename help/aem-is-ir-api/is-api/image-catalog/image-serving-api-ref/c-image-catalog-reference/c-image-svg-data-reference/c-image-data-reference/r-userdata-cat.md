---
description: 用户数据。 服务器会将此字段的内容返回给客户端，以响应req=userdata。
solution: Experience Manager
title: 用户数据
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# 用户数据{#userdata}

用户数据。 服务器会将此字段的内容返回给客户端，以响应req=userdata。

## 属性 {#section-06f2002b77d54a64be07f12fff54ad13}

文本字符串值。 建议使用 [属性数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 格式化。 如果未使用属性数据格式，则文本字符串不得包含“=”字符。

缩放、旋转和小册子查看器客户端假定此字段使用属性数据格式。 这些客户端使用此字段进行查看器配置和自定义。 有关详细信息，请参阅查看器文档。

此字段参与文本字符串本地化。 请参阅 [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP协议参考* 了解详细信息。

## 默认 {#section-7ee879762130467199745f2abc662f1e}

无。

## 另请参阅 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
