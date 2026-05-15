---
description: 映像服务组件由服务器监控程序管理，它是Linux守护程序或Windows服务（S7Supervisor.exe，在服务控制面板中列为“Dynamic Media映像服务”）。
solution: Experience Manager
title: 服务器主管
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
TQID: 'https://experienceleague.adobe.com/D3cGGQLVly7MwWSvSjkWcWkuR9kVUFC9sSvItZm6eOc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# 服务器主管{#server-supervisor}

映像服务组件由服务器监控程序管理，它是Linux守护程序或Windows服务（S7Supervisor.exe，在服务控制面板中列为“Dynamic Media映像服务”）。

除了启动和停止其他图像服务组件之外，服务器管理员还负责确保这些其他组件的运行状况。 如果组件崩溃，它会自动重新启动，以将任何服务中断降至最低。

## 启动和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

使用图像服务实用程序脚本启动、停止和重新启动服务器主管。 有关详细信息，请参阅[实用工具文档](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

启动和停止服务器监控器会自动启动和停止所有其他图像服务组件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
