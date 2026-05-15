---
description: 存在图像。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
TQID: 'https://experienceleague.adobe.com/JyGNYH5-vW7FbZbMcMk2mQFB7rrrzYd0FpvsBbI-Zi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# 存在{#exists}

存在图像。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`*&#x200B;唯一请求标识符

返回名为`catalogRecord.exists`的单个属性。 如果图像或默认目录中存在指定的目录条目，则属性值设置为“1”，否则属性值设置为“0”。 针对`/is/content`上下文的`req=exists`请求指示静态内容目录中是否存在指定记录。

请求字符串中的其他命令将被忽略。 可使用基于`attribute::NonImgExpiration`的TTL来缓存HTTP响应。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选. 默认值为`s7jsonResponse`。
