---
description: 在嵌入的外部请求的花括号中出现的$var$引用将替换为匹配的变量定义值。
solution: Experience Manager
title: 嵌入式外来请求中的变量处理
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# 嵌入式外来请求中的变量处理{#variable-processing-in-embedded-foreign-requests}

在嵌入的外部请求的花括号中出现的$var$引用将替换为匹配的变量定义值。

这允许将嵌入的外来请求放置在图像目录中的模板中。

要替换为外部请求的变量值通常必须进行多次编码，因为在服务器尝试传输最终的外部url之前，不会应用重新编码。
