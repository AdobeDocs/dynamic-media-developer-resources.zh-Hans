---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '154'
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
   * `eventInfo {String}` 事件裝載。

另請參閱 [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md)和 [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
