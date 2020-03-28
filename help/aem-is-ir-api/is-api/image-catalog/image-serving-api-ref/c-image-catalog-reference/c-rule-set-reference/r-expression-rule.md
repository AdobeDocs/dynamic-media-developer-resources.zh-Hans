---
description: 常规表达式图案元素。 在<rule>元素中为可选。
seo-description: 常规表达式图案元素。 在<rule>元素中为可选。
seo-title: 表达式
solution: Experience Manager
title: 表达式
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 表达式{#expression}

常规表达式图案元素。 元素中为可 `<rule>` 选。

## 属性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

无。

## 数据 {#section-e2601008d71243109af1a8c55b58416d}

常规表达式模式字符串。

## 说明 {#section-759bfb738ddb45dba1f0807aba8c1113}

元 `<expression>` 素可以是空的或包含简单的搜索字符串或常规表达式模式。 该模式将应用于整个请求字符串。

匹配始终在空或未 `<expression>` 指定时发生；这等同于指定 `<expression>.*</expression>`。

该实现基于Java包 [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)，它提供与Perl类似的常规表达式语法。

## 说明 {#section-10b472a902674893b49ca49a7052c366}

表达式字符串不能包含文本&lt;和&amp;字符。 这些保留字符可以分别用 `&` 和 `<`编码，或者整个字符串可以包含在XML部 `CDATA` 分中：

`<expression><![CDATA[&fmt=custom]]></expression>`

标签和标签之间的所 `<expression>` 有字符 `</expression>` 都会传递给常规表达式分析器，包括可选部分之外的字符 `CDATA` 。 应当注意避免出现额外的空白。

## 另请参阅 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
