---
description: 属性数据由表示一个或多个属性的文本字符串组成。
solution: Experience Manager
title: 属性数据
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 属性数据{#property-data}

属性数据由表示一个或多个属性的文本字符串组成。

属性由属性名称和属性值组成，以=分隔。

多个属性通过行分隔符分隔，行分隔符可以是`??`或`<CR><LF>`。 如果整个属性数据字符串未用引号括起来，则服务器会在将数据发送到客户端之前，将每个出现的`??`替换为`<CR><LF>`。 属性名称可以由字母、数字、“。”、“ — ”和“_”组成。 属性名称不区分大小写。

属性值不得包含行分隔符。

有关应用于属性数据的其他规则，请参阅[文本字符串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
