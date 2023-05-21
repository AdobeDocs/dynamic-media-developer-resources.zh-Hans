---
description: 替代字串元素。 選填於 <rule> 元素。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# 替代{#substitution}

替代字串元素。 選填於 `<rule>` 元素。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

无。

## 数据 {#section-a2688866ed6d41279a8478886e511ae3}

替代字串。

## 说明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

為路徑或查詢中的相符字串或子字串定義取代字串。

如果模式運算式包含子運算式（以括弧分隔），則第一個相符的子字串會被取代字串所取代。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

若 `<expression>` 為空白或不存在，則會將替代字串附加至路徑或查詢。

若 `<substitution>` 空白，則會移除相符的字串或子字串。 若 `<substitution>` 未指定，路徑或查詢字串未修改。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可編碼為 `&` 和 `<`，或者整個字串可以包含在XML中 `CDATA` 區段：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
