---
description: 事件回调
solution: Experience Manager
title: 事件回调
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

回调处理程序通过传递事件名称和相应的处理程序函数(使用 `handlers` 属性 `config` 查看器构造函数中的JSON对象。 或者，也可以使用 `setHandlers()` API方法。

支持的查看器事件包括：

* `initComplete`  — 在查看器初始化完成并创建所有内部组件时触发，以便能够使用 `getComponent()` API。 回调处理程序不接受任何参数。

* `trackEvent`  — 每次在查看器内发生事件时触发，事件可能由事件跟踪系统(如Adobe Analytics)处理。 回调处理程序采用以下参数：

   * `objID {String}` 当前未使用。
   * `compClass {String}` 当前未使用。
   * `instName {String}` 触发事件的查看器SDK组件的实例名称。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负载。

另请参阅 [SmartCropVideoViewer]
(../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0)和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
