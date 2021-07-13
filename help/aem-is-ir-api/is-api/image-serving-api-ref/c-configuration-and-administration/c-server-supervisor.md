---
description: 映像服务组件由服务器管理员管理，服务器管理员是Linux后台程序或Windows服务(S7Supervisor.exe，在“服务”控制面板中列为“Dynamic Media映像服务”)。
solution: Experience Manager
title: 服务器主管
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 服务器主管{#server-supervisor}

映像服务组件由服务器管理员管理，服务器管理员是Linux后台程序或Windows服务(S7Supervisor.exe，在“服务”控制面板中列为“Dynamic Media映像服务”)。

除了启动和停止其他图像服务组件外，服务器主管还负责确保这些其他组件的运行状况。 如果组件发生崩溃，将自动重新启动组件以最大限度地减少任何服务中断。

## 启动和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

使用图像服务实用程序脚本启动、停止和重新启动服务器管理器。 有关更多信息，请参阅[实用工具文档](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

启动和停止服务器管理器将自动启动和停止所有其他图像服务组件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
