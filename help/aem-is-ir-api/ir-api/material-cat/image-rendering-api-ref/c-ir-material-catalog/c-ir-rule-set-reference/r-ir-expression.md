---
description: 正则表达式模式元素。 <rule>元素中的可选。
solution: Experience Manager
title: 表达式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 4%

---

# 表达式{#expression}

正则表达式模式元素。 `<rule>`元素中的可选。

## 属性 {#section-fd0574eee1f9423cbb2ed709c0906800}

无。

## 数据 {#section-4cd740c511a1432da0955e9acfbcf96f}

正则表达式模式字符串。

## 说明 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>`元素可以为空或包含简单搜索字符串或正则表达式模式。 该模式将应用于整个请求字符串。

当`<expression>`为空或未指定时，始终会发生匹配；这等同于指定`<expression>.*</expression>`。

该实现基于Java包[java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)，它提供了与Perl类似的正则表达式语法。

## 注意 {#section-6b41a900b0ce4a9590e5861e3c81599c}

表达式字符串不得包含文本&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`和`</expression>`标记之间的所有字符都将传递到正则表达式分析器，包括可选`CDATA`部分之外的字符。 应小心避免留出额外的空格。

## 另请参阅 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)

