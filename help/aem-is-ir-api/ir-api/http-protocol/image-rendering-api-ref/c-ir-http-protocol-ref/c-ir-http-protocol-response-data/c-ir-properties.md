---
title: 属性
description: 属性数据是作为对以下req=类型imageprops和prop的响应返回的。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 属性{#properties}

作为对以下req=类型的响应，返回属性数据： imageprops和props。

回复数据的格式设置为可读为Java™属性。 典型的文本属性响应具有以下常规结构：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*`可以为空。 在每行的开始和结束位置以及“=”分隔符之前和之后，空格是可选的。 可以使用单引号或双引号将字符串值括起来，但不是必需的。

字符串值可以包含JAVA样式转义字符，如`\n`、`\t`、`\:`或`\\`。

**另请参阅**

[需要=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
