---
title: 事件回调
description: 事件回调
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 68aa55da-5f6f-4c7d-8d3f-c25de9cc325c
TQID: 'https://experienceleague.adobe.com/sVoOBxs4zuGoZKBa3bjwBQQ2ga4AFMCKWdtF0GKOzvs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

回调处理程序是通过将事件名称和相应的处理程序函数与`handlers`属性一起传递给查看器的构造函数中的`config` JSON对象来分配的。 或者，也可以使用`setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete` — 查看器初始化完成并创建所有内部组件时触发，以便可以使用`getComponent()` API。 回调处理程序不接受任何参数。

* `trackEvent` — 每次在查看器中发生事件时都会触发，该事件可能由事件跟踪系统（如Adobe Analytics）处理。 回调处理程序采用以下参数：

   * `objID {String}`当前未使用。
   * `compClass {String}`当前未使用。
   * `instName {String}`触发事件的查看器SDK组件的实例名称。
   * `timeStamp {Number}`事件时间戳。
   * `eventInfo {String}`事件有效负载

另请参阅[ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
