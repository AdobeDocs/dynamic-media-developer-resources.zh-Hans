---
description: 命令值必须使用%xx转义序列进行http编码，以便值字符串不包含保留字符“=”、“&”和“%”。
solution: Experience Manager
title: 图像渲染HTTP编码
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# 图像渲染HTTP编码{#image-rendering-http-encoding}

命令值必须使用%xx转义序列进行http编码，以便值字符串不包含保留字符“=”、“&amp;”和“%”。

否则，将应用标准HTTP编码规则。 HTTP规范要求对不安全字符(如“（空格）”、“”（双引号）、“#”、“%”、“&lt;”和“>”)以及任何控制字符（如`<return>`和`<tab>`）进行编码。

**注意：** 不得对用作请求嵌套分隔符的大括号{ }进行编码。遗憾的是，某些电子邮件客户端在嵌入的HTTP请求中对大括号进行编码。 如果是这个问题，图像渲染允许使用圆括号()而不是大括号。

## 示例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述请求片段必须进行如下编码：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另请参阅 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1规范(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
