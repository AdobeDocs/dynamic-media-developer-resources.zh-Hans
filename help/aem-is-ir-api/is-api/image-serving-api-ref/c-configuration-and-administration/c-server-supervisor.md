---
description: 映像服务组件由服务器监控器管理，服务器监控器是Linux守护程序或Windows服务(S7Supervisor.exe，在服务控制面板中列为“Dynamic Media映像服务”)。
solution: Experience Manager
title: 服务器主管
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 服务器主管{#server-supervisor}

映像服务组件由服务器监控器管理，服务器监控器是Linux守护程序或Windows服务(S7Supervisor.exe，在服务控制面板中列为“Dynamic Media映像服务”)。

除了启动和停止其他图像服务组件之外，服务器管理员还负责确保这些其他组件的运行状况。 如果组件崩溃，则会自动重新启动，以将任何服务中断降至最低。

## 启动和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

使用图像服务实用程序脚本启动、停止和重新启动服务器监控器。 请参阅 [实用程序文档](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) 了解更多信息。

启动和停止服务器监控器会自动启动和停止所有其他图像服务组件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
