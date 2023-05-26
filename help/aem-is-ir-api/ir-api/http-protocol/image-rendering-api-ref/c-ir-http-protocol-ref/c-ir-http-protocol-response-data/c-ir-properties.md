---
title: 属性
description: 响应以下req=类型imageprop和prop返回属性数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---

# 属性{#properties}

响应以下req=类型返回属性数据： imageprops和props。

回复数据的格式可读为Java™属性。 典型的文本属性响应具有以下常规结构：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以为空。 在每行的开始和结束位置以及“=”分隔符之前和之后，可选使用空格。 可以使用单引号或双引号来括住字符串值，但不是必需的。

字符串值可以包含JAVA样式转义字符，例如 `\n`， `\t`， `\:`，或 `\\`.

**另请参阅**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
