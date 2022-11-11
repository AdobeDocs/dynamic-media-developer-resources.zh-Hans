---
description: 针对CDN失效请求中提供的一个URL响应的详细消息。
solution: Experience Manager
title: 操作故障
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

---

# [!DNL OperationFault]{#operationfault}

针对CDN失效请求中提供的一个URL响应的详细消息。

**支持时间**

4.5.0，修补程序2011-02

## 参数 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名称** | ** 类型** | ** 说明** |
|---|---|---|
| 代码 | `xsd:int` | 从CDN提供的错误代码 |
| 原因 | `xsd:string` | 从CDN提供的错误消息 |
