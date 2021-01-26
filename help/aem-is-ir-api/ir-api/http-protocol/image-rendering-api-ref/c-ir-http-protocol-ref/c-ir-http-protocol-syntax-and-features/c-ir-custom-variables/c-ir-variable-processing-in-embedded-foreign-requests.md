---
description: 嵌入的外部请求的花括号中出现的$var$引用将替换为匹配的变量定义值。
seo-description: 嵌入的外部请求的花括号中出现的$var$引用将替换为匹配的变量定义值。
seo-title: 嵌入式外部请求中的变量处理
solution: Experience Manager
title: 嵌入式外部请求中的变量处理
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# 嵌入式外部请求中的变量处理{#variable-processing-in-embedded-foreign-requests}

嵌入的外部请求的花括号中出现的$var$引用将替换为匹配的变量定义值。

这允许将嵌入的外来请求放入图像目录的模板中。

要替换为外部请求的变量值通常必须进行多次编码，因为在服务器尝试传输最终的外部url之前，不会应用重新编码。
