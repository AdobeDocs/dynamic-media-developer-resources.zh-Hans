---
description: 事件回调
solution: Experience Manager
title: 事件回调
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

通过将具有`handlers`属性的事件名和相应的处理函数传递给查看器的构造函数中的`config` JSON对象，为回调处理函数赋值。 或者，也可以使用`setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete`  — 查看器初始化完成并创建所有内部组件时触发，以便能够使用 `getComponent()` API。回调处理函数不采用任何参数。

* `trackEvent`  — 每次在查看器内发生事件时触发，该查看器可由事件跟踪系统(如Adobe Analytics)处理。回调处理函数采用以下参数：

   * `objID {String}` 当前未使用。
   * `compClass {String}` 当前未使用。
   * `instName {String}` 触发事件的查看器SDK组件的实例名。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负荷。

另请参阅[ eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)。
