---
title: 常見資料型別
description: 目錄屬性和欄位可能包含下列其中一種型別的資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# 常見資料型別{#common-data-types}

目錄屬性和欄位可能包含下列其中一種型別的資料。

**颜色**

色彩值。 十六進位、封包RGB值，可選擇以0x開頭。 例如，RGB值 `128,255,0` 可指定為 `0x80ff00` 或 `80ff00`.

**标记**

`0`=false， `1`=true，任何其他值都表示未知或未指定。

**列舉**

`0` 表示未知或未指定的值，與空白欄位相同。 有效 `enum` 值是從1開始的連續整數。

**整數**

帶正負號的整數值(例如 `0, -12, 34`)。 `0` 或負值可能有特殊意義。

**實數**

帶正負號的浮點值(例如， `0, 12.5, 245 , -2.34e4`)。 0或負值可能有特殊意義。

**文字字串**

字串分隔符號為選用，除非字串包含 `<CR>`， `<LF>`，或 `<TAB>` 個字元。 單引號與雙引號均可作為分隔符號使用。 如果使用引號，則內嵌在字串中的任何引號都必須使用兩個連續引號來逸出(例如， `This month''s Special`&#39;)。
