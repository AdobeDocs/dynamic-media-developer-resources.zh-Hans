---
title: 图像
description: 如果请求成功完成，并且请求不包含req=命令，或者req=具有以下值之一img，则返回图像数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令或req=具有以下值之一，则会返回图像数据： img、debug

HTTP响应MIME类型由 `fmt=`，或者，如果 `fmt=` 未指定，它取决于 `attribute::Format`.

如果请求方法是无条件的，则HTTP响应状态为“200 OK” `GET` 或 `HEAD`.

服务器可以状态“304”（未修改）回复，并且不响应条件返回任何图像数据 `GET` 请求(使用 [!DNL If-Modified-Since] 字段中存在 `request-header`)。
