---
description: 对CDN失效请求中提供的URL做出响应的详细消息。
seo-description: 对CDN失效请求中提供的URL做出响应的详细消息。
seo-title: OperationFault
solution: Experience Manager
title: OperationFault
topic: Dynamic Media Image Production System API
uuid: 879d025b-3269-4f87-b8bd-b7916509d077
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 9%

---


# OperationFault{#operationfault}

对CDN失效请求中提供的URL做出响应的详细消息。

**支持时间**

4.5.0，修补程序2011-02

## 参数 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名称** | ** 类型** | ** 说明** |
|---|---|---|
| `*`代码`*` | `xsd:int` | 从CDN提供的错误代码 |
| `*`原因`*` | `xsd:string` | 从CDN提供的错误消息 |

