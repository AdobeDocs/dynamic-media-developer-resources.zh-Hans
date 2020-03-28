---
description: 调试请求。 此调试命令可解析和预处理请求、执行图像目录查找、目录修饰符包含、宏和变量替换等，如req=img。
seo-description: 调试请求。 此调试命令可解析和预处理请求、执行图像目录查找、目录修饰符包含、宏和变量替换等，如req=img。
seo-title: 解决
solution: Experience Manager
title: 解决
topic: Scene7 Image Serving - Image Rendering API
uuid: bd1576a7-4802-4a87-b1c0-406f51382561
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 解决{#resolve}

调试请求。 此调试命令会分析并预处理请求，执行图像目录查找， catalog::Modifier inclusion，宏和变量替换等，就像req=img一样。

`req=resolve`

将返回最终的请求字符串，而不是MIME类型的结果图像 `text/plain`。

HTTP响应不可缓存。
