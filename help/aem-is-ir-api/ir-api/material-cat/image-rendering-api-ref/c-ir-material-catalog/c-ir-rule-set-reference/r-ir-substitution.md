---
title: 替换
description: 替换字符串元素。 <rule>元素中的可选。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 替换{#substitution}

替换字符串元素。 `<rule>`元素中的可选。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

无。

## 数据 {#section-a2688866ed6d41279a8478886e511ae3}

替换字符串。

## 说明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

为路径或查询中匹配的字符串或子字符串定义替换字符串。

如果模式表达式包含子表达式（用括号分隔），则第一个匹配的子字符串将被替换为替换字符串。 如果模式表达式不包含子表达式，则将替换整个匹配的字符串。

如果`<expression>`为空或不存在，则替代字符串将附加到路径或查询中。

如果`<substitution>`为空，则将删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不会修改路径或查询字符串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替换字符串不得包含文字&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
