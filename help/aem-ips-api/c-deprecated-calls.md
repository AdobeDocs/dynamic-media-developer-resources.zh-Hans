---
title: 已弃用的调用
description: 不再在Dynamic Media中使用的图像生产系统API调用及其关联参数。
solution: Experience Manager
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# 已弃用的调用{#deprecated-calls}

不再使用的图像生产系统API调用及其关联参数。

## 已弃用的调用{#topic-654c0466e6434fe4a95953322255b08c}

不再在Dynamic Media中使用的图像生产系统API调用及其关联参数。

* `addMediaPortalEvent`  — 操作中已弃用。此调用允许您向IPS添加媒体门户事件。
* `getMediaPortalEvent`  — 操作中已弃用。通过此调用，您可以获得符合指定条件的媒体门户事件。
* `getCdnCacheInvalidationStatus`  — 操作中已弃用。此API现已弃用，因为`cdnCacheInvalidation` API几乎立即使缓存无效（~5秒）。 因此，不再需要轮询失效状态。

