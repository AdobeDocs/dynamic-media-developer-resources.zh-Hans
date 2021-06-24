---
title: 已弃用的调用
description: 不再在Dynamic Media中使用的图像生产系统API调用及其关联参数。
solution: Experience Manager
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 已弃用的调用{#deprecated-calls}

不再使用的图像生产系统API调用及其关联参数。

## 已弃用的调用 {#topic-654c0466e6434fe4a95953322255b08c}

不再在Dynamic Media中使用的图像生产系统API调用及其关联参数。

* `addMediaPortalEvent`  — 操作中已弃用。此调用允许您向IPS添加媒体门户事件。
* `getMediaPortalEvent`  — 操作中已弃用。此调用允许您获取与指定标准匹配的媒体门户事件。
* `getCdnCacheInvalidationStatus`  — 操作中已弃用。此API现已弃用，因为`cdnCacheInvalidation` API几乎立即使缓存失效（约5秒）。 因此，不再需要轮询失效状态。
