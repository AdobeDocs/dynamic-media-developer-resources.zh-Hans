---
description: 如果将文本指定为响应格式，则返回数据的格式化为可读为Java属性。
solution: Experience Manager
title: 文本(Java)属性
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 文本(Java)属性{#text-java-properties}

如果将文本指定为响应格式，则返回数据的格式化为可读为Java属性。

典型的文本属性响应具有以下通用结构：

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

*`propertyValue`* 可能为空。在每行的开头和结尾以及=分隔符前后的空格都是可选的。 可以使用单引号或双引号引住字符串值，但不是必需的。

字符串值可能包含JAVA样式的转义字符，如`\n`、`\t`、`\:`或`\\`。
