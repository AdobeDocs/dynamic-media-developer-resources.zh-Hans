---
description: 规则表达式图案元素。 在<rule>元素中为可选。
seo-description: 规则表达式图案元素。 在<rule>元素中为可选。
seo-title: 表达式
solution: Experience Manager
title: 表达式
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 4%

---


# 表达式{#expression}

规则表达式图案元素。 在`<rule>`元素中为可选。

## 属性 {#section-fd0574eee1f9423cbb2ed709c0906800}

无。

## 数据 {#section-4cd740c511a1432da0955e9acfbcf96f}

常规表达式模式字符串。

## 说明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`元素可以是空的，也可以包含简单的搜索字符串或常规表达式模式。 该模式将应用于整个请求字符串。

当`<expression>`为空或未指定时，始终会发生匹配；这等效于指定`<expression>.*</expression>`。

该实现基于Java包[java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)，它提供与Perl类似的常规表达式语法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

表达式字符串不能包含文本&lt;和&amp;字符。 这些保留字符可以分别用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`标记之间的所有字符都会传递到常规表达式分析器，包括可选`CDATA`部分外的字符。 应当注意避免额外的空白。

## 另请参阅 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
