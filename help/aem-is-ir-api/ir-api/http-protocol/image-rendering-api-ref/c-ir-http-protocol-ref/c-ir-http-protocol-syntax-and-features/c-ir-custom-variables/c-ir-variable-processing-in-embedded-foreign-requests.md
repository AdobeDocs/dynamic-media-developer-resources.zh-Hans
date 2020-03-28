---
description: 嵌入的外部请求的花括号内发生的$var$引用将替换为匹配的变量定义值。
seo-description: 嵌入的外部请求的花括号内发生的$var$引用将替换为匹配的变量定义值。
seo-title: 嵌入式外来请求中的变量处理
solution: Experience Manager
title: 嵌入式外来请求中的变量处理
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 嵌入式外来请求中的变量处理{#variable-processing-in-embedded-foreign-requests}

嵌入的外部请求的花括号内发生的$var$引用将替换为匹配的变量定义值。

这允许将嵌入的外来请求放入图像目录的模板中。

要替换为外来请求的变量值通常必须采用多次编码，因为在服务器尝试传输最终的外来url之前，不会应用重新编码。
