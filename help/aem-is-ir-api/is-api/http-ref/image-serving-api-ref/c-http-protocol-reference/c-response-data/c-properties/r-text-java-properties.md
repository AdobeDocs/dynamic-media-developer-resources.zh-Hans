---
description: 如果将文本指定为响应格式，则返回数据的格式设置为可读为Java属性。
seo-description: 如果将文本指定为响应格式，则返回数据的格式设置为可读为Java属性。
seo-title: 文本(Java)属性
solution: Experience Manager
title: 文本(Java)属性
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# 文本(Java)属性{#text-java-properties}

如果将文本指定为响应格式，则返回数据的格式设置为可读为Java属性。

典型的文本属性响应具有以下常规结构：

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

*`propertyValue`* 可能是空的。在每行的开头和结尾以及=分隔符前后，空格是可选的。 单引号或多次引号可用于圈起字符串值，但不是必需的。

字符串值可能包含JAVA样式转义字符，如`\n`、`\t`、`\:`或`\\`。
