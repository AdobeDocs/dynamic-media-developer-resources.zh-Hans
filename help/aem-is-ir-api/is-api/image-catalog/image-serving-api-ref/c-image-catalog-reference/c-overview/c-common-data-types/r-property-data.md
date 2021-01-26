---
description: 属性数据由表示一个或多个属性的文本字符串组成。
seo-description: 属性数据由表示一个或多个属性的文本字符串组成。
seo-title: 属性数据
solution: Experience Manager
title: 属性数据
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# 属性数据{#property-data}

属性数据由表示一个或多个属性的文本字符串组成。

属性由属性名和属性值组成，以=分隔。

多个属性由行分隔符分隔，行分隔符可以是`??`或`<CR><LF>`。 如果整个属性数据字符串没有用引号引起来，则服务器会在将数据传输到客户端之前用`<CR><LF>`替换每个出现的`??`。 属性名称可能由字母、数字、“.”、“-”和“_”组成。 属性名称不区分大小写。

属性值不能包括行分隔符。

有关应用于属性数据的其他规则，请参阅[文本字符串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)。
