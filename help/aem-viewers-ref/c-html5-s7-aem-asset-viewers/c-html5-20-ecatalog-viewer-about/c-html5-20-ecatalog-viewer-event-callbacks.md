---
description: 'null'
seo-description: 'null'
seo-title: 事件回调
solution: Experience Manager
title: 事件回调
topic: Dynamic media
uuid: 8afb5a98-45f2-4319-bece-70c27f0f68dc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 事件回调{#event-callbacks}

查看器支持JavaScript事件回调，网页使用它跟踪查看器初始化过程或运行时行为。

回调处理函数通过将事件名和相应的处理函数与属性传递 `handlers` 给查看器的构造 `config` 函数中的JSON对象来分配。 或者，也可以使用 `setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete` -查看器初始化完成并创建所有内部组件时触发器，以便能够使用 `getComponent()` API。 回调处理函数不采用任何参数。

* `trackEvent` -每次在查看器中发生事件时触发，该查看器可由事件跟踪系统（如Adobe Analytics）处理。 回调处理函数采用以下参数：

   * `objID {String}` 当前未使用。
   * `compClass {String}` 当前未使用。
   * `instName {String}` 触发事件的查看器SDK组件的实例名。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负荷。

另请参 [阅eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
