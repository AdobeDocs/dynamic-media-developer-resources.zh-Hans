---
description: 如果请求成功完成，并且请求中不包含req=命令，或req=包含以下值之一，则返回图像数据img，调试
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# 图像{#images}

如果请求成功完成，并且请求中不包含req=命令，或req=包含以下值之一，则返回图像数据：img，调试

HTTP响应MIME类型由`fmt=`确定，或者，如果未指定`fmt=`，则取决于`attribute::Format`的值。

如果请求方法为无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可以以状态“304”（未修改）回复，并且不返回任何图像数据以响应条件`GET`请求（`request-header`中存在[!DNL If-Modified-Since]字段）。
