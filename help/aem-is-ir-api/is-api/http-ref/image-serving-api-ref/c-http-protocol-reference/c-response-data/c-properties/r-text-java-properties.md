---
description: 如果指定文本作为响应格式，则回复数据的格式将设置为可读的Java属性。
solution: Experience Manager
title: 文本(Java)属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 文本(Java)属性{#text-java-properties}

如果指定文本作为响应格式，则回复数据的格式将设置为可读的Java属性。

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

*`propertyValue`*&#x200B;可能为空。 在每行的开始和结束位置以及=分隔符之前和之后，空格是可选的。 可以使用单引号或双引号将字符串值括起来，但不是必需的。

字符串值可以包含JAVA样式转义字符，如`\n`、`\t`、`\:`或`\\`。
