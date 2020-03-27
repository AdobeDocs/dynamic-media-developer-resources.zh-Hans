---
description: 命令值必须使用%xx转义序列进行http编码，这样值字符串中就不包括保留字符'='、'&'和'%'。
seo-description: 命令值必须使用%xx转义序列进行http编码，这样值字符串中就不包括保留字符'='、'&'和'%'。
seo-title: 图像渲染HTTP编码
solution: Experience Manager
title: 图像渲染HTTP编码
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 图像渲染HTTP编码{#image-rendering-http-encoding}

命令值必须使用%xx转义序列进行http编码，这样值字符串中就不包括保留字符&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;。

否则，将应用标准HTTP编码规则。 HTTP规范要求对“（空格）”、“”(多次引号)、“#”、“%”、“&lt;”和“>”等不安全字符以及任何控制字符（如和）进行编 `<return>` 码 `<tab>`。

**注意：** 用作请求嵌套分隔符的大括号{ }不能进行编码。 某些电子邮件客户端不幸地在嵌入的HTTP请求中编码大括号。 如果这是问题，图像渲染允许使用括号()而不是大括号。

## 示例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述请求片段必须按照以下方式进行编码：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另请参阅 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1规范(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
