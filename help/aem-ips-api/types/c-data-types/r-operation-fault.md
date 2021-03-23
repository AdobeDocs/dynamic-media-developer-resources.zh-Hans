---
description: 对CDN失效请求中提供的URL作出响应的详细消息。
seo-description: 对CDN失效请求中提供的URL作出响应的详细消息。
seo-title: OperationFault
solution: Experience Manager
title: OperationFault
uuid: 879d025b-3269-4f87-b8bd-b7916509d077
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---


# OperationFault{#operationfault}

对CDN失效请求中提供的URL作出响应的详细消息。

**支持时间**

4.5.0，修补程序2011-02

## 参数 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名称** | ** 类型** | ** 说明** |
|---|---|---|
| `*`代码`*` | `xsd:int` | 从CDN提供的错误代码 |
| `*`原因`*` | `xsd:string` | 从CDN提供的错误消息 |

