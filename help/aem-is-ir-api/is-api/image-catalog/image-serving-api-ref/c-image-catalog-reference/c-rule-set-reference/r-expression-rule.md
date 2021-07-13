---
description: 正则表达式模式元素。 在<rule>元素中为可选项。
solution: Experience Manager
title: 表达式
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# 表达式{#expression}

正则表达式模式元素。 在`<rule>`元素中为可选。

## 属性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

无。

## 数据 {#section-e2601008d71243109af1a8c55b58416d}

正则表达式模式字符串。

## 说明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`元素可以为空，也可以包含简单的搜索字符串或正则表达式模式。 该模式将应用于整个请求字符串。

当`<expression>`为空或未指定时，始终会出现匹配；这等同于指定`<expression>.*</expression>`。

该实施基于Java包[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)，该包提供与Perl类似的正则表达式语法。

## 说明 {#section-10b472a902674893b49ca49a7052c366}

表达式字符串不得包含文字&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`标记之间的所有字符都将传递到正则表达式解析器，包括可选`CDATA`部分外的字符。 应当注意避免出现额外的空格。

## 另请参阅 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
