---
description: 如果请求成功完成，并且请求不包含req=命令或req=img或req=tmb，则会返回图像数据。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# 图像{#images}

如果请求成功完成，并且请求不包含req=命令或req=img或req=tmb，则会返回图像数据。

HTTP响应MIME类型由`fmt=`确定，如果未指定`fmt=`，则它为`<image/jpeg>`。

如果请求方法是无条件的`GET`或`HEAD`，则HTTP响应状态为“200 OK”。

服务器可能会以状态“304”（未修改）回复，并且不会返回任何图像数据以响应条件性`GET`请求（包括有效的`If-Modified-Since`或`If-None-Match`标头）。
