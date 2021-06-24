---
description: 如果请求成功完成，并且请求不包含req=命令，或者req=img或req=tmb，则返回图像数据。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令，或者req=img或req=tmb，则返回图像数据。

HTTP响应MIME类型由`fmt=`确定，或者，如果未指定`fmt=`，则为`<image/jpeg>`。

如果请求方法是无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可以以状态“304”（未修改）进行回复，并且不返回任何图像数据以响应条件性`GET`请求（包括有效的`If-Modified-Since`或`If-None-Match`标头）。
