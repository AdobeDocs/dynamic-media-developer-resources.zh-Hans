---
title: 已弃用的调用
description: ' [!DNL Dynamic Media]中不再使用或支持的图像生产系统API调用及其关联参数。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 已弃用的调用{#deprecated-calls}

不再使用的图像生产系统API调用及其关联参数。

## 已弃用的调用 {#topic-654c0466e6434fe4a95953322255b08c}

不再在[!DNL Dynamic Media]中使用的图像生产系统API调用及其关联参数。

* `ExcludeMasterVideoFromAVS` — 已弃用[数据类型](/help/aem-ips-api/types/c-data-types/c-data-types.md)。 此参数从自适应视频集中排除主视频。<!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` — 已弃用[操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 此参数允许您将Media Portal事件添加到IPS。
* `getMediaPortalEvent` — 已弃用[操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 此参数允许您获取与指定条件匹配的Media Portal事件。
* `getCdnCacheInvalidationStatus` — 已弃用[操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md)。 此参数现在已被弃用，因为`cdnCacheInvalidation`参数几乎立即使缓存失效（约5秒）。 因此，不再需要轮询失效状态。
