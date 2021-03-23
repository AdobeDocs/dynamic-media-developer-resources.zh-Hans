---
description: 命令值必须使用%xx转义序列进行http编码，以使值字符串不包括保留字符“=”、“&”和“%”。
seo-description: 命令值必须使用%xx转义序列进行http编码，以使值字符串不包括保留字符“=”、“&”和“%”。
seo-title: 图像渲染HTTP编码
solution: Experience Manager
title: 图像渲染HTTP编码
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# 图像渲染HTTP编码{#image-rendering-http-encoding}

命令值必须使用%xx转义序列进行http编码，以使值字符串不包括保留字符“=”、“&amp;”和“%”。

否则，将应用标准HTTP编码规则。 HTTP规范要求对“（空格）”、“”(多次引号)、“#”、“%”、“&lt;”和“>”等不安全字符以及任何控制字符（如`<return>`和`<tab>`）进行编码。

**注意：** 不能对用作请求嵌套分隔符的花括号{ }进行编码。不幸的是，某些电子邮件客户端会在嵌入的HTTP请求中对花括号进行编码。 如果这是问题，图像渲染允许使用圆括号()而不是花括号。

## 示例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述请求片段必须进行如下编码：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另请参阅 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1规范(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
