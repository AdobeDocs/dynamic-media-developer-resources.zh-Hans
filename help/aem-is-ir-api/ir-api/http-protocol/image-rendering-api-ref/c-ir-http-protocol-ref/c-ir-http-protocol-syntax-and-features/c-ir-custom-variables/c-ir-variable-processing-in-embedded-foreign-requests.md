---
title: 在嵌入的外来请求中进行变量处理
description: 在嵌入的外来请求的大括号内的任何位置出现的$var$引用将被匹配的变量定义值替换。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 在嵌入的外来请求中进行变量处理{#variable-processing-in-embedded-foreign-requests}

在嵌入的外来请求的大括号内的任何位置出现的任何`$var$`引用都将替换为匹配的变量定义值。

允许将嵌入的外部请求放置在图像目录的模板中。

要替换到外地请求中的变量值通常必须经过双重编码，因为在服务器尝试传输最终的外部url之前不会应用重新编码。
