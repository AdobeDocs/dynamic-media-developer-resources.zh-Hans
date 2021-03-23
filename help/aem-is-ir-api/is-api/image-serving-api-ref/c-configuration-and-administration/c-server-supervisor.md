---
description: 图像服务组件由服务器主管管理，服务器主管是Linux守护程序或Windows服务(S7Supervisor.exe，在“服务”控制面板中列为“Dynamic Media图像服务”)。
seo-description: 图像服务组件由服务器主管管理，服务器主管是Linux守护程序或Windows服务(S7Supervisor.exe，在“服务”控制面板中列为“Dynamic Media图像服务”)。
seo-title: 服务器主管
solution: Experience Manager
title: 服务器主管
uuid: 6ac38d90-00ed-4d49-84f0-2e77e7a86d47
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# 服务器管理器{#server-supervisor}

图像服务组件由服务器主管管理，服务器主管是Linux守护程序或Windows服务(S7Supervisor.exe，在“服务”控制面板中列为“Dynamic Media图像服务”)。

除了启动和停止其他图像服务组件，服务器主管还负责确保这些其他组件的运行状况。 如果组件发生崩溃，将自动重新启动它以最大限度地减少任何服务中断。

## 启动和停止{#section-061d28d74e034a30adc39ea3e2031cd0}

服务器管理器将启动、停止，并使用图像服务实用程序脚本重新启动。 有关详细信息，请参阅[实用程序文档](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)。

启动和停止Server Supervisor会自动开始和停止所有其他图像服务组件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
