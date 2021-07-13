---
description: 调试请求。 此调试命令会解析并预处理请求、执行图像目录查找、目录修饰符包含、宏和变量替换等，如req=img。
solution: Experience Manager
title: 解决
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---

# 解决{#resolve}

调试请求。 此调试命令会解析并预处理请求、执行图像目录查找、目录：：修饰符包含、宏和变量替换等，如req=img。

`req=resolve`

返回最终的请求字符串，而不是结果图像，其MIME类型为`text/plain`。

无法缓存HTTP响应。
