---
title: 图像
description: 如果请求成功完成，并且请求不包含req=命令或req=具有以下值之一img、debug，则会返回图像数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令或req=具有以下值之一，则会返回图像数据： img、debug

HTTP响应MIME类型由`fmt=`确定，如果未指定`fmt=`，则它依赖于`attribute::Format`的值。

如果请求方法是无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可能会以状态“304”（未修改）回复，并且不会返回任何图像数据以响应条件性`GET`请求（在`request-header`中存在[!DNL If-Modified-Since]字段）。
