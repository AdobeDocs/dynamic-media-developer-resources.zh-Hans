---
title: 图像渲染HTTP编码
description: 命令值必须使用%xx转义序列进行http编码，以便值字符串不包含保留字符“=”、“&”和“%”。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
TQID: 'https://experienceleague.adobe.com/TNB9NbrGzMGS64CxHgj7aXlSHz8-KPBB0hMxB36mKvI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# 图像渲染HTTP编码{#image-rendering-http-encoding}

命令值必须使用%xx转义序列进行http编码，以便值字符串不包含保留字符“=”、“&amp;”和“%”。

否则，将应用标准HTTP编码规则。 HTTP规范要求对不安全的字符(如“ ”（空格）、“ ”（双引号）、“#”、“%”、“&lt;”和“>”)以及任何控制字符（如`<return>`和`<tab>`）进行编码。

**注意：**&#x200B;用作请求嵌套分隔符的大括号{ }不能编码。 很遗憾，某些电子邮件客户端会在嵌入HTTP请求中编码大括号。 如果出现此问题，图像渲染允许使用括号( )而不是大括号。

## 示例 {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

上述请求片段必须按如下方式进行编码：

`…&$text=rate%26weight%3D85%25%2027%23&…`

## 另请参阅 {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1规范(RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)

