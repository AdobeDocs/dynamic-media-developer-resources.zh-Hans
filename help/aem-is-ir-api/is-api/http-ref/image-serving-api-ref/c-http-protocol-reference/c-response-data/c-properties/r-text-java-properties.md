---
description: 如果将文本指定为响应格式，则返回数据的格式将设置为可读为Java属性。
seo-description: 如果将文本指定为响应格式，则返回数据的格式将设置为可读为Java属性。
seo-title: 文本(Java)属性
solution: Experience Manager
title: 文本(Java)属性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# 文本(Java)属性{#text-java-properties}

如果将文本指定为响应格式，则返回数据的格式将设置为可读为Java属性。

典型文本属性响应具有以下一般结构：

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* 可能是空的。在每行的开始和结尾以及=分隔符前后，空白是可选的。 单引号或多次引号可用于圈住字符串值，但不是必需的。

字符串值可能包含JAVA样式转义字符，如`\n`、`\t`、`\:`或`\\`。
