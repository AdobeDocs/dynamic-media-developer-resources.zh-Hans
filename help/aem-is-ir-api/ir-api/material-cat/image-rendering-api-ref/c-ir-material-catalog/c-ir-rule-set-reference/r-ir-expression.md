---
description: 正则表达式模式元素。 可选，位于 <rule> 元素。
solution: Experience Manager
title: 表达式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# 表达式{#expression}

正则表达式模式元素。 可选，位于 `<rule>` 元素。

## 属性 {#section-fd0574eee1f9423cbb2ed709c0906800}

无。

## 数据 {#section-4cd740c511a1432da0955e9acfbcf96f}

正则表达式模式字符串。

## 说明 {#section-3245c8a531bb455d8398449f6ea63b37}

此 `<expression>` 元素可以为空或包含简单搜索字符串或正则表达式模式。 该模式将应用于整个请求字符串。

在以下情况下，始终会发生匹配 `<expression>` 为空或未指定；这等同于指定 `<expression>.*</expression>`.

该实施基于Java包 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)，提供与Perl类似的正则表达式语法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

表达式字符串不得包含文字&lt;和&amp;字符。 这些保留字符可使用进行编码 `&` 和 `<`，或者整个字符串可以包含在XML中 `CDATA` 部分：

`<expression><![CDATA[&fmt=custom]]></expression>`

以下字符之间的所有字符 `<expression>` 和 `</expression>` 标记将传递到正则表达式解析器，包括可选字符之外的字符 `CDATA` 部分。 应小心避免留出额外的空格。

## 另请参阅 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
