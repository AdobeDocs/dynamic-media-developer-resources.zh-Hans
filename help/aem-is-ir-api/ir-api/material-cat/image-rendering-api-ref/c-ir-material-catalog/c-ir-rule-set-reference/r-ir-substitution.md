---
description: 替换字符串元素。 在<rule>元素中为可选。
seo-description: 替换字符串元素。 在<rule>元素中为可选。
seo-title: 替代
solution: Experience Manager
title: 替代
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
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

如果模式表达式包括子表达式（用括号分隔），则用替换字符串替换第一个匹配的子字符串。 如果模式表达式不包括子表达式，则替换整个匹配字符串。

如果`<expression>`为空或不存在，则替换字符串会附加到路径或查询。

如果`<substitution>`为空，则删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不修改路径或查询字符串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替换字符串不得包含文本&lt;和&amp;字符。 这些保留字符可以分别用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
