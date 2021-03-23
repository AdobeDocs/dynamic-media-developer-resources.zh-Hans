---
description: 事件回调
solution: Experience Manager
title: 事件回调
uuid: 1b9af9e4-463a-4982-9e81-681ebebfd6d7
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
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

另请参阅[BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9)。
