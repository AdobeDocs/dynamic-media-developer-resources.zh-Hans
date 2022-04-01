---
title: 已弃用的调用
description: 不再在Dynamic Media中使用或支持的图像生产系统API调用及其关联参数。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 72f9cd1b1de82cbeeb8d41fb0f1cf0b51744a8a3
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# 已弃用的调用{#deprecated-calls}

不再使用的图像生产系统API调用及其关联参数。

## 已弃用的调用 {#topic-654c0466e6434fe4a95953322255b08c}

不再在Dynamic Media中使用的图像生产系统API调用及其关联参数。

* `ExcludeMasterVideoFromAVS`  — 从 [数据类型](/help/aem-ips-api/types/c-data-types/c-data-types.md). 此参数从自适应视频集中排除主视频。 <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent`  — 从 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 通过此参数，可向IPS添加媒体门户事件。
* `getMediaPortalEvent`  — 从 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 通过此参数，您可以获取与指定标准匹配的媒体门户事件。
* `getCdnCacheInvalidationStatus`  — 从 [操作](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 此参数现已弃用，因为 `cdnCacheInvalidation` 参数几乎立即使缓存失效（约5秒）。 因此，不再需要轮询失效状态。
