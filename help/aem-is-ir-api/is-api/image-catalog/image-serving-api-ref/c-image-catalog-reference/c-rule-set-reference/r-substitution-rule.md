---
description: 替代字串元素。 選填於 <rule> 元素。
solution: Experience Manager
title: 替代
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# 替代{#substitution}

替代字串元素。 選填於 `<rule>` 元素。

## 属性 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

无。

## 数据 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

替代字串。

## 说明 {#section-4a64a93f5e1a4d04a2db19166578bf76}

為路徑或查詢中的相符字串或子字串定義取代字串。

如果模式運算式包含子運算式（以括弧分隔），則第一個相符的子字串會取代為替代字串。 如果模式運算式不包含子運算式，則會取代整個相符的字串。

若 `<expression>` 為空白或不存在，則會將替代字串附加至路徑或查詢。

若 `<substitution>` 空白，則會移除相符的字串或子字串。 若 `<substitution>` 未指定，路徑或查詢字串未修改。

>[!NOTE]
>
>在下列情況下，輸入字串中的所有相符專案都會被取代： `replace="all"` 指定於 `<rule>`，此專案所屬的元素 `<substitution>` 元素所屬的。 依預設，只有第一個相符專案會取代為替代字串。

## 注意 {#section-cedf2adabaaf441c9f598fb0ea180246}

替代字串不得包含常值&lt;和&amp;字元。 這些保留字元可編碼為 `&` 和 `<`，或是整個字串可以包含在XML CDATA區段中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
