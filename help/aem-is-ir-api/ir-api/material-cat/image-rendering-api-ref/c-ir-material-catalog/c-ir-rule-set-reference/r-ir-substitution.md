---
description: 替换字符串元素。 在<rule>元素中为可选项。
solution: Experience Manager
title: 替换
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# 替换{#substitution}

替换字符串元素。 在`<rule>`元素中为可选。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

无。

## 数据 {#section-a2688866ed6d41279a8478886e511ae3}

替换字符串。

## 说明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

为路径或查询中的匹配字符串或子字符串定义替换字符串。

如果模式表达式包含子表达式（用圆括号分隔），则第一个匹配的子字符串将替换为替换字符串。 如果模式表达式不包含子表达式，则将替换整个匹配的字符串。

如果`<expression>`为空或缺失，则替换字符串会附加到路径或查询中。

如果`<substitution>`为空，则删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不会修改路径或查询字符串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替换字符串不得包含文字&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
