---
title: 解决
description: 调试请求。 此调试命令可解析并预处理请求、执行图像目录查找、目录修饰符包含、宏和变量替换等，就像req=img一样。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# 解决{#resolve}

调试请求。 此调试命令可解析并预处理请求、执行图像目录查找、catalog：：Modifier包含、宏和变量替换等，就像req=img一样。

`req=resolve`

返回的是MIME类型为`text/plain`的最终请求字符串，而不是结果图像。

无法缓存HTTP响应。
