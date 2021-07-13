---
description: 事件回调
solution: Experience Manager
title: 事件回调
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

在查看器的构造函数中，通过将事件名称和具有`handlers`属性的相应处理程序函数传递到`config` JSON对象，来分配回调处理程序。 或者，也可以使用`setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete`  — 在查看器初始化完成并创建所有内部组件时触发，以便能够使用 `getComponent()` API。回调处理程序不接受任何参数。

* `trackEvent`  — 每次在查看器内发生事件时触发，事件可能由事件跟踪系统(如Adobe Analytics)处理。回调处理程序采用以下参数：

   * `objID {String}` 当前未使用。
   * `compClass {String}` 当前未使用。
   * `instName {String}` 触发事件的查看器SDK组件的实例名称。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负载。

另请参阅[BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9)。
