---
description: 事件回调
solution: Experience Manager
title: 事件回调
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '221'
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

* `quickViewActivate`  — 当用户在交互式色板组件中或视频播放结束时显示的“行动动员”屏幕中单击或点按交互式色板时触发。回调处理函数采用唯一具有以下字段的JSON对象参数：

   * `sku` {  `String`}与交互式色板关联的SKU值。
   * `<additionalVariable>` {  `String`}零个或多个与交互式色板关联的其他变量。

另请参阅[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
