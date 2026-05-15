---
description: 如果指定文本作为响应格式，则回复数据的格式将设置为可读的Java属性。
solution: Experience Manager
title: 文本(Java)属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
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
