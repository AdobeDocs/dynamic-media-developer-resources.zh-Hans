---
title: 常见数据类型
description: 目录属性和字段可能包含以下类型之一的数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# 常见数据类型{#common-data-types}

目录属性和字段可能包含以下类型之一的数据。

**颜色**

颜色值。 十六进制的RGB值，前面可选为0x。 例如，RGB值 `128,255,0` 可以指定为 `0x80ff00` 或 `80ff00`.

**标记**

`0`=false， `1`=true，则任何其他值表示未知或未指定。

**枚举**

`0` 指示未知或未指定的值，与空字段相同。 有效 `enum` 值是从1开始的连续整数数。

**整数**

带符号的整数值(例如 `0, -12, 34`)。 `0` 或负值可能具有特殊含义。

**实数**

带符号的浮点值(例如， `0, 12.5, 245 , -2.34e4`)。 0或负值可能具有特殊含义。

**文本字符串**

字符串分隔符是可选的，除非字符串包含任何 `<CR>`, `<LF>`或 `<TAB>` 字符。 单引号和双引号均可用作分隔符。 如果使用引号，则嵌入在字符串中的任何此类引号都必须使用两个连续的引号(例如，&#39; `This month''s Special`&#39;)。
