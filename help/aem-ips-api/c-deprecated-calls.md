---
description: 不再使用的Image Production System API调用及其关联参数。
seo-description: 不再使用的Image Production System API调用及其关联参数。
seo-title: 已弃用的调用
solution: Experience Manager
title: 已弃用的调用
topic: Scene7 Image Production System API
uuid: 03925728-f011-45f0-84a6-808dff0fd529
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 已弃用的调用{#deprecated-calls}

不再使用的Image Production System API调用及其关联参数。

## 已弃用的调用 {#topic-654c0466e6434fe4a95953322255b08c}

不再使用的Image Production System API调用及其关联参数。

* `addMediaPortalEvent` -操作中已弃用。 此调用允许您向IPS添加媒体门户事件。
* `getMediaPortalEvent` -操作中已弃用。 通过此调用，您可以获得符合指定条件的媒体门户事件。
* `getCdnCacheInvalidationStatus` -操作中已弃用。 此API现已弃用，因为 `cdnCacheInvalidation` API几乎立即使缓存无效（约5秒）。 因此，不再需要轮询失效状态。

