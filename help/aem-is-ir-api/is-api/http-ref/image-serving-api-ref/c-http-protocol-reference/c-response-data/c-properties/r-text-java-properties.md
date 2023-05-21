---
description: 如果將文字指定為回應格式，則會將回覆資料格式化為可讀取的Java屬性。
solution: Experience Manager
title: 文字(Java)屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 文字(Java)屬性{#text-java-properties}

如果將文字指定為回應格式，則會將回覆資料格式化為可讀取的Java屬性。

典型的文字屬性回應具有此一般結構：

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

*`propertyValue`* 可能是空的。 每行開頭和結尾以及=分隔符號之前和之後的空白字元為選用。 可以使用單引號或雙引號來括住字串值，但並非必要。

字串值可包含JAVA樣式的逸出字元，例如 `\n`， `\t`， `\:`，或 `\\`.
