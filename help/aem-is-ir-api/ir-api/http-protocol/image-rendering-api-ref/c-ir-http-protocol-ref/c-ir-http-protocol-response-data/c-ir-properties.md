---
description: 属性数据将返回，以响应以下req=类型imageprop和prop。
seo-description: 属性数据将返回，以响应以下req=类型imageprop和prop。
seo-title: 属性
solution: Experience Manager
title: 属性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# 属性{#properties}

属性数据会根据以下req=类型返回：imageprops和props。

回复数据的格式设置为可读为Java属性。 典型文本属性响应具有以下一般结构：

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 可以是空的。在每行的开始和结尾以及“=”分隔符前后，空白是可选的。 单引号或多次引号可用于圈住字符串值，但不是必需的。

字符串值可能包含JAVA样式转义字符，如`\n`、`\t`、`\:`。 或者 `\\`.

**另请参阅**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
