---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行階段行為的JavaScript事件回呼。

回呼處理常式是透過傳遞事件名稱和對應的處理常式函式來指派 `handlers` 屬性至 `config` 檢視器建構函式中的JSON物件。 或者，也可以使用 `setHandlers()` api方法。

支援的檢視器事件包括：

* `initComplete`  — 當檢視器初始化完成並建立所有內部元件時觸發，以便使用 `getComponent()` API。 回呼處理常式不接受任何引數。

* `trackEvent`  — 每次在檢視器內發生事件時都會觸發，事件追蹤系統可能會處理(例如Adobe Analytics)。 回呼處理常式會採用下列引數：

   * `objID {String}` 目前未使用。
   * `compClass {String}` 目前未使用。
   * `instName {String}` 觸發事件之Viewer SDK元件的執行個體名稱。
   * `timeStamp {Number}` 事件時間戳記。
   * `eventInfo {String}` 事件裝載。

另請參閱 [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) 和 [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
