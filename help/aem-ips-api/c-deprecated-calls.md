---
title: 已弃用的调用
description: 不再在Dynamic Media使用的图像生产系统API调用及其关联参数。
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 已弃用的调用{#deprecated-calls}

不再使用的图像生产系统API调用及其关联参数。

## 已弃用的调用{#topic-654c0466e6434fe4a95953322255b08c}

不再在Dynamic Media使用的图像生产系统API调用及其关联参数。

* `addMediaPortalEvent` -操作中已弃用。此调用允许您向IPS添加媒体门户事件。
* `getMediaPortalEvent` -操作中已弃用。此调用可让您获得符合指定条件的媒体门户事件。
* `getCdnCacheInvalidationStatus` -操作中已弃用。此API现已弃用，因为`cdnCacheInvalidation` API几乎立即使缓存失效（~5秒）。 因此，不再需要轮询失效状态。

