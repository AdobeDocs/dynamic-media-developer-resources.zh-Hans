---
title: img
description: 图像（默认）。 请求标准图像数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 22%

---

# img{#img}

图像（默认）。 请求标准图像数据。

`req=img`

回复数据格式和响应MIME类型由确定 `fmt=`. 修饰符 `req=img` 是默认的请求类型，不需要显式使用。 HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他请求命令将按文档所述应用。
