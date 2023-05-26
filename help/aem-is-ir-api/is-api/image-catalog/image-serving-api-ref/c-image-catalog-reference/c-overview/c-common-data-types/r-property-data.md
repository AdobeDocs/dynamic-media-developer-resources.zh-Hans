---
description: 属性数据由表示一个或多个属性的文本字符串组成。
solution: Experience Manager
title: 属性数据
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# 属性数据{#property-data}

属性数据由表示一个或多个属性的文本字符串组成。

属性由属性名称和属性值组成，以=分隔。

多个属性由行分隔符分隔，该分隔符可以是 `??` 或 `<CR><LF>`. 如果整个属性数据字符串未用引号括起来，则服务器将替换出现的每个 `??` 替换为 `<CR><LF>` 将数据传输到客户端之前。 属性名称可以包含字母、数字、“。”、“ — ”和“_”。 属性名称不区分大小写。

属性值不得包含行分隔符。

参见 [文本字符串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) 以了解应用于属性数据的其他规则。
