---
description: 替换字符串元素。 在<rule>元素中为可选。
seo-description: 替换字符串元素。 在<rule>元素中为可选。
seo-title: 替代
solution: Experience Manager
title: 替代
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# 替换{#substitution}

替换字符串元素。 在`<rule>`元素中为可选。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

无。

## 数据 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替换字符串。

## 说明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

为路径或查询中的匹配字符串或子字符串定义替换字符串。

如果模式表达式包括子表达式（用括号分隔），则用替换字符串替换第一个匹配的子字符串。 如果模式表达式不包括子表达式，则替换整个匹配字符串。

如果`<expression>`为空或不存在，则替换字符串会附加到路径或查询。

如果`<substitution>`为空，则删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不修改路径或查询字符串。

>[!NOTE]
>
>当在此`<substitution>`元素所属的`<rule>`元素中指定`replace="all"`时，将替换输入字符串中的所有匹配项。 默认情况下，只有第一个匹配项被替换为替换字符串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替换字符串不能包含文本&lt;和&amp;字符。 这些保留字符可以分别用`&`和`<`进行编码，或者整个字符串可以包含在XML CDATA部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
