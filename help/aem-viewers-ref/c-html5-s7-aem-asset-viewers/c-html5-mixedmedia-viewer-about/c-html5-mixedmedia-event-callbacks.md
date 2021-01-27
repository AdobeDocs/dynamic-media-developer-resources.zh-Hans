---
description: 事件回调
solution: Experience Manager
title: 事件回调
topic: Dynamic Media
uuid: 696838d2-11e4-4ef8-9cd3-136c5d5f6ed9
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

回调处理函数的分配方法是将具有`handlers`属性的事件名和相应的处理函数传递给查看器的构造函数的`config` JSON对象。 或者，也可以使用`setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete` -查看器初始化完成并创建所有内部组件时触发，以便可以使用 `getComponent()` API。回调处理函数不采用任何参数。

* `trackEvent` -每次在查看器中发生事件时都触发，该事件跟踪系统可能会处理该事件，如Adobe Analytics。回调处理函数采用以下参数：

   * `objID {String}` 当前未使用。
   * `compClass {String}` 当前未使用。
   * `instName {String}` 触发事件的查看器SDK组件的实例名称。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负荷。

另请参阅[MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3)。
