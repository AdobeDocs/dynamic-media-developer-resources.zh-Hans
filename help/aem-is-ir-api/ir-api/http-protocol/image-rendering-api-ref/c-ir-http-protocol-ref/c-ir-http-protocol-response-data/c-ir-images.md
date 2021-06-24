---
description: 如果请求成功完成，并且请求不包含req=命令，或者req=具有以下值之一，则会返回图像数据img， debug。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令，或者req=具有以下值之一，则返回图像数据：img，调试

HTTP响应MIME类型由`fmt=`确定，或者，如果未指定`fmt=`，则取决于`attribute::Format`的值。

如果请求方法是无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可以以状态“304”（未修改）进行回复，并且不返回任何图像数据以响应条件性`GET`请求（[!DNL If-Modified-Since]字段位于`request-header`中）。
