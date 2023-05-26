---
description: 预加载服务器缓存。 执行请求的方式与req=img类似，但服务器不会返回图像，而是返回回复图像的长度(image.length)，格式为带有MIME类型text/plain的文本数据。
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# loadcache{#loadcache}

预加载服务器缓存。 执行请求的方式与req=img类似，但服务器不会返回图像，而是返回回复图像的长度(image.length)，格式为带有MIME类型text/plain的文本数据。

`req=loadcache`

无法缓存HTTP响应。

请求中的其他命令将按文档所述应用。
