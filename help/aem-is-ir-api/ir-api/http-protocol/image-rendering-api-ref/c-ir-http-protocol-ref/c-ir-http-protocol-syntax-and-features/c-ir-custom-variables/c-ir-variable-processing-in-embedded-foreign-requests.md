---
title: 嵌入式外来请求中的变量处理
description: 嵌入的外来请求的大括号内出现的$var$引用将被匹配的变量定义值替换。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 嵌入式外来请求中的变量处理{#variable-processing-in-embedded-foreign-requests}

任意 `$var$` 嵌入的外来请求的大括号内出现的引用将被匹配的变量定义值替换。

允许将嵌入的外来请求放置在图像目录的模板中。

要替换为外来请求的变量值通常必须进行双重编码，因为在服务器尝试传输最终的外来URL之前，不会应用重新编码。
