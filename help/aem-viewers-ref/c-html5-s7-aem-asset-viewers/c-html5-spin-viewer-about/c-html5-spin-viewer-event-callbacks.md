---
description: 事件回调
solution: Experience Manager
title: 事件回调
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
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

另请参阅[SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef)。
