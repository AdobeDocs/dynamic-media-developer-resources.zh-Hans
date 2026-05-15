---
title: 在嵌入的外来请求中进行变量处理
description: 在嵌入的外来请求的大括号内的任何位置出现的$var$引用将被匹配的变量定义值替换。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# 在嵌入的外来请求中进行变量处理{#variable-processing-in-embedded-foreign-requests}

在嵌入的外来请求的大括号内的任何位置出现的任何`$var$`引用都将替换为匹配的变量定义值。

允许将嵌入的外部请求放置在图像目录的模板中。

要替换到外地请求中的变量值通常必须经过双重编码，因为在服务器尝试传输最终的外部url之前不会应用重新编码。
