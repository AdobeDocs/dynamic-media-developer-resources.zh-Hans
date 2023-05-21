---
description: 「影像伺服」元件是由「伺服器監督員」所管理，它是Linux精靈或Windows服務(S7Supervisor.exe，列為「服務控制面板」中的「Dynamic Media影像伺服」)。
solution: Experience Manager
title: 伺服器監督員
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 83b6a63f-6bb8-4a14-b8d5-389d23fae57c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 伺服器監督員{#server-supervisor}

「影像伺服」元件是由「伺服器監督員」所管理，它是Linux精靈或Windows服務(S7Supervisor.exe，列為「服務控制面板」中的「Dynamic Media影像伺服」)。

除了啟動和停止其他「影像伺服」元件外，伺服器監督員還負責確保這些其他元件的健康狀態。 如果元件當機，則會自動重新啟動，以將任何服務中斷降至最低。

## 啟動和停止 {#section-061d28d74e034a30adc39ea3e2031cd0}

伺服器監督員會使用「影像伺服」公用程式指令碼啟動、停止和重新啟動。 請參閱 [公用程式檔案](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) 以取得詳細資訊。

啟動和停止Server Supervisor會自動啟動和停止所有其他的「影像伺服」元件。

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
