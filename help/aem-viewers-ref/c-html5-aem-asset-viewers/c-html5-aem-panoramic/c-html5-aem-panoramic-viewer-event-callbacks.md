---
title: 事件回调
description: 事件回调
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '143'
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
   * `instName {String}` 触发事件的HTML5查看器SDK组件的实例名称。
   * `timeStamp {Number}` 事件时间戳。
   * `eventInfo {String}` 事件有效负载。

