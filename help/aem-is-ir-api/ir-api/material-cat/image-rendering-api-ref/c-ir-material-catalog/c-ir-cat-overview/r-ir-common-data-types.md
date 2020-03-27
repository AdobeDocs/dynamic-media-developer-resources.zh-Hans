---
description: 目录属性和字段可能包含下列类型之一的数据。
seo-description: 目录属性和字段可能包含下列类型之一的数据。
seo-title: 常见数据类型
solution: Experience Manager
title: 常见数据类型
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 常见数据类型{#common-data-types}

目录属性和字段可能包含下列类型之一的数据。

**颜色**

颜色值。 十六进制的压缩RGB值，可选前面有0x。 例如，RGB值可 `128,255,0` 以指定为 `0x80ff00` 或 `80ff00`。

**标记**

`0`=false, `1`=true，任何其他值表示未知或未指定。

**Enum**

0表示未知或未指定的值，与空字段相同。 有效 `enum` 值是连续的整数，以1开头。

**整数**

带符号的整数值（例如0、-12、34）。 0或负值可能具有特殊含义。

**实数**

已签名浮点值(例如 `0, 12.5, 245 , -2.34e4`)。 0或负值可能具有特殊含义。

**文本字符串**

字符串分隔符是可选的，除非字符串包含任何 `<CR>`、 `<LF>`或字符 `<TAB>` 。 单引号和多次引号均可用作分隔符。 如果使用引号，则嵌入在字符串中的任何此类引号必须使用两个连续的引号(例如，&#39; `This month''s Special`&#39;)。
