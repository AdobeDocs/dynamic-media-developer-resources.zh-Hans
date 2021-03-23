---
description: 如果请求成功完成，并且请求中不包含req=命令，或req=包含以下值之一，则返回图像数据img，调试
seo-description: 如果请求成功完成，并且请求中不包含req=命令，或req=包含以下值之一，则返回图像数据img，调试
seo-title: 图像
solution: Experience Manager
title: 图像
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# 图像{#images}

如果请求成功完成，并且请求中不包含req=命令，或req=包含以下值之一，则返回图像数据：img，调试

HTTP响应MIME类型由`fmt=`确定，或者，如果未指定`fmt=`，则取决于`attribute::Format`的值。

如果请求方法为无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可以以状态“304”（未修改）回复，并且不返回任何图像数据以响应条件`GET`请求（`request-header`中存在[!DNL If-Modified-Since]字段）。
