---
description: 如果请求成功完成，并且请求中不包含req=命令，或req=img或req=tmb，则返回图像数据。
seo-description: 如果请求成功完成，并且请求中不包含req=命令，或req=img或req=tmb，则返回图像数据。
seo-title: 图像
solution: Experience Manager
title: 图像
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像{#images}

如果请求成功完成，并且请求中不包含req=命令，或req=img或req=tmb，则返回图像数据。

HTTP响应MIME类型由 `fmt=`或者，如果未 `fmt=` 指定，则由它确定 `<image/jpeg>`。

如果请求方法为无条件或，则HTTP响应状态为“200 `GET` OK” `HEAD`。

服务器可以以状态“304”（未修改）回复，并且不返回任何图像数据以响应条件请 `GET` 求(包括有效或头 `If-Modified-Since` 部 `If-None-Match` )。
