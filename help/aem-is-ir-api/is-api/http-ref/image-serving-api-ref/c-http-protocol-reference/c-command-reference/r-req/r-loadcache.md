---
description: 预加载服务器缓存。 执行请求的方式与req=img类似，但服务器不会返回图像，而是返回回复图像的长度(image.length)，格式为带有MIME类型text/plain的文本数据。
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
TQID: 'https://experienceleague.adobe.com/Llp-0huLGkxBVxSgRngyAtNKqeHuZ02xJu71MM-Nqww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# loadcache{#loadcache}

预加载服务器缓存。 执行请求的方式与req=img类似，但服务器不会返回图像，而是返回回复图像的长度(image.length)，格式为带有MIME类型text/plain的文本数据。

`req=loadcache`

无法缓存HTTP响应。

请求中的其他命令将按文档所述应用。
