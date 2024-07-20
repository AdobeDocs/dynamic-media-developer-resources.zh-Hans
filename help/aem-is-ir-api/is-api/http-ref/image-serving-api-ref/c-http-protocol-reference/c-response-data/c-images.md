---
description: 如果请求成功完成，并且请求不包含req=命令或req=img或req=tmb，则会返回图像数据。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令或req=img或req=tmb，则会返回图像数据。

HTTP响应MIME类型由`fmt=`确定，如果未指定`fmt=`，则它为`<image/jpeg>`。

如果请求方法是无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可能会以状态“304”（未修改）回复，并且不会返回任何图像数据以响应条件性`GET`请求（包括有效的`If-Modified-Since`或`If-None-Match`标头）。
