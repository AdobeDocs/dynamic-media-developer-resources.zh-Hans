---
title: 常见数据类型
description: 目录属性和字段可能包含下列类型之一的数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 常见数据类型{#common-data-types}

目录属性和字段可能包含下列类型之一的数据。

**颜色**

颜色值。 十六进制、打包的RGB值，也可以选择以0x开头。 例如，RGB值`128,255,0`可以指定为`0x80ff00`或`80ff00`。

**标志**

`0`=false，`1`=true，任何其他值表示未知或未指定。

**枚举**

`0`表示未知或未指定的值，与空字段相同。 有效的`enum`值是从1开始的连续整数。

**整数**

带符号的整数值（例如`0, -12, 34`）。 `0`或负值可能有特殊含义。

**实数**

带符号的浮点值（例如，`0, 12.5, 245 , -2.34e4`）。 0或负值可能具有特殊含义。

**文本字符串**

字符串分隔符是可选的，除非字符串包含任何`<CR>`、`<LF>`或`<TAB>`字符。 单引号和双引号均可用作分隔符。 如果使用引号，则字符串中嵌入的任何此类引号必须使用两个连续的引号进行转义（例如，“`This month''s Special`”）。

