---
description: 属性数据会返回以响应以下req=类型imageprops和prop。
seo-description: 属性数据会返回以响应以下req=类型imageprops和prop。
seo-title: 属性
solution: Experience Manager
title: 属性
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# 属性{#properties}

属性数据会返回以下req=类型：imageprops和props。

回复数据的格式设置为可读为Java属性。 典型的文本属性响应具有以下常规结构：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以是空的。在每行的开头和结尾以及“=”分隔符前后，空格是可选的。 单引号或多次引号可用于圈起字符串值，但不是必需的。

字符串值可能包含JAVA样式转义字符，如`\n`、`\t`、`\:`。 或者 `\\`.

**另请参阅**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
