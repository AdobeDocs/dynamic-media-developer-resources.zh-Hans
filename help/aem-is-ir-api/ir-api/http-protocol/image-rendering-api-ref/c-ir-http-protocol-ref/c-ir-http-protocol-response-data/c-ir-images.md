---
description: 如果请求成功完成，并且请求中不包含req=命令，或req=具有下列值之一，则返回图像数据img，调试
seo-description: 如果请求成功完成，并且请求中不包含req=命令，或req=具有下列值之一，则返回图像数据img，调试
seo-title: 图像
solution: Experience Manager
title: 图像
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像{#images}

如果请求成功完成，并且请求中不包含req=命令，或者req=具有以下值之一，则返回图像数据：img，调试

HTTP响应MIME类型由 `fmt=`或者，如 `fmt=` 果未指定，则取决于的值 `attribute::Format`。

如果请求方法为无条件或，则HTTP响应状态为“200 `GET` OK” `HEAD`。

服务器可以以状态“304”（未修改）回复，并且不返回任何图像数据以响应条件请 `GET` 求(该字段 [!DNL If-Modified-Since] 在中存在 `request-header`)。
