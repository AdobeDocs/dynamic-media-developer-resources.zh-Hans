---
description: 'null'
seo-description: 'null'
seo-title: 事件回调
solution: Experience Manager
title: 事件回调
topic: Dynamic media
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
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

另请参 [阅SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef)。
