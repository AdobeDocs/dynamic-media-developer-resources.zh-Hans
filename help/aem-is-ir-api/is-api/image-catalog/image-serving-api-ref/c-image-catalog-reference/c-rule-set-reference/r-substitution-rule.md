---
description: 替换字符串元素。 <rule>元素中的可选。
solution: Experience Manager
title: 替换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# 替换{#substitution}

替换字符串元素。 `<rule>`元素中的可选。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

无。

## 数据 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替换字符串。

## 说明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

为路径或查询中匹配的字符串或子字符串定义替换字符串。

如果模式表达式包含子表达式（用圆括号分隔），则第一个匹配的子字符串将被替换为替换字符串。 如果模式表达式不包含子表达式，则将替换整个匹配的字符串。

如果`<expression>`为空或不存在，则替代字符串将附加到路径或查询中。

如果`<substitution>`为空，则将删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不会修改路径或查询字符串。

>[!NOTE]
>
>在此`replace="all"`元素所属的`<rule>`，元素中指定了`<substitution>`时，输入字符串中的所有匹配项都会被替换。 默认情况下，只有第一个匹配项会被替换为替换字符串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替换字符串不得包含文字&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML CDATA部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
