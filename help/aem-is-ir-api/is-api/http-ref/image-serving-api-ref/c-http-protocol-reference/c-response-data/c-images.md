---
description: 如果请求成功完成，并且请求中不包含req=命令，或req=img或req=tmb，则返回图像数据。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---


# 图像{#images}

如果请求成功完成，并且请求中不包含req=命令，或req=img或req=tmb，则返回图像数据。

HTTP响应MIME类型由`fmt=`确定，或者，如果未指定`fmt=`，则为`<image/jpeg>`。

如果请求方法为无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可以以状态“304”（未修改）回复，并且不返回任何图像数据以响应条件`GET`请求（包括有效的`If-Modified-Since`或`If-None-Match`头）。
