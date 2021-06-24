---
description: 用户数据. 服务器响应req=userdata，将此字段的内容返回给客户端。
solution: Experience Manager
title: 用户数据
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 8%

---

# 用户数据{#userdata}

用户数据. 服务器响应req=userdata，将此字段的内容返回给客户端。

## 属性 {#section-06f2002b77d54a64be07f12fff54ad13}

文本字符串值。 建议使用[属性数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)格式。 如果不使用属性数据格式，则文本字符串不得包含“=”字符。

缩放、旋转和手册查看器客户端假定此字段使用资产数据格式。 这些客户端使用此字段进行查看器配置和自定义。 有关详细信息，请参阅查看器文档。

此字段参与文本字符串本地化。 有关详细信息，请参阅&#x200B;*HTTP协议引用*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 默认 {#section-7ee879762130467199745f2abc662f1e}

无。

## 另请参阅 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ，文 [本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
