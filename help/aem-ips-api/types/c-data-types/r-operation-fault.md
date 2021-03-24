---
description: 对CDN失效请求中提供的URL作出响应的详细消息。
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

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

