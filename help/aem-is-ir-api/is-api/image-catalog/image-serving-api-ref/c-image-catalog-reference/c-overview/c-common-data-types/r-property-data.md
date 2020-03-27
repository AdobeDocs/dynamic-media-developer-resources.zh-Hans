---
description: 属性数据由表示一个或多个属性的文本字符串组成。
seo-description: 属性数据由表示一个或多个属性的文本字符串组成。
seo-title: 属性数据
solution: Experience Manager
title: 属性数据
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 属性数据{#property-data}

属性数据由表示一个或多个属性的文本字符串组成。

属性由属性名称和属性值组成，以=分隔。

多个属性由行分隔符分隔，行分隔符可以是 `??` 或 `<CR><LF>`。 如果整个属性数据字符串没有用引号括起来，则服务器在将数据发送到客户端之前， `??` 会 `<CR><LF>` 将每个出现的属性替换为。 属性名称可能由字母、数字、&#39;.&#39;、&#39;-&#39;和&#39;_&#39;组成。 属性名称不区分大小写。

属性值不得包括行分隔符。

有关应 [用于属性数据的其他规则](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) ，请参阅文本字符串。
