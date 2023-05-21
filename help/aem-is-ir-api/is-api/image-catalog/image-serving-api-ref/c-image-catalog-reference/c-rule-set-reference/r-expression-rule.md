---
description: 規則運算式模式元素。 選填於 <rule> 元素。
solution: Experience Manager
title: 運算式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 4%

---

# 運算式{#expression}

規則運算式模式元素。 選填於 `<rule>` 元素。

## 属性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

无。

## 数据 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 说明 {#section-759bfb738ddb45dba1f0807aba8c1113}

此 `<expression>` 元素可以空白，或包含簡單搜尋字串或規則運算式模式。 此模式會套用至整個請求字串。

符合專案一律發生於 `<expression>` 為空白或未指定；這相當於指定 `<expression>.*</expression>`.

實作以Java套件為基礎 [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)，提供類似Perl的規則運算式語法。

## 说明 {#section-10b472a902674893b49ca49a7052c366}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可編碼為 `&` 和 `<`，或者整個字串可以包含在XML中 `CDATA` 區段：

`<expression><![CDATA[&fmt=custom]]></expression>`

所有介於「 」和「 」之間 `<expression>` 和 `</expression>` 標籤會傳遞至規則運算式剖析器，包括選擇性以外的字元 `CDATA` 區段。 請務必小心避免出現額外的空格。

## 另请参阅 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
