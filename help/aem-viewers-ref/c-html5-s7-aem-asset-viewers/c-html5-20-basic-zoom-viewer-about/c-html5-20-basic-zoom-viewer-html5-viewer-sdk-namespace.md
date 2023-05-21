---
title: 檢視器SDK名稱空間
description: 檢視器SDK名稱空間
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4ccdf8c2-6cf5-4cb3-af61-fab50f410566
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# 檢視器SDK名稱空間{#viewer-sdk-namespace}

檢視器是由許多Viewer SDK元件所建置。 通常網頁不需要直接與SDK元件API互動；所有常見需求都包含在檢視器API本身中。

不過，有些進階使用案例會要求網頁參考使用下列專案的內部SDK元件： `getComponent()` 檢視器API，然後使用SDK本身的API的所有彈性。

檢視器用來載入及初始化SDK元件的名稱空間取決於檢視器運作的環境。 如果檢視器是在Adobe Experience Manager中執行，則檢視器會將SDK元件載入到 `s7viewers.s7sdk` 名稱空間。 而Dynamic Media Classic提供的檢視器會將SDK載入 `s7classic.s7sdk`.

在任一情況下，檢視器內SDK使用的名稱空間會有 `s7viewers` 或 `s7classic` 作為前置詞。 而且，它與一般情況不同 `s7sdk` SDK使用手冊或SDK API檔案中使用的名稱空間。

因此，當您撰寫與內部檢視器元件通訊的自訂應用程式程式碼時，使用完整限定的SDK名稱空間非常重要。

例如，如果您計畫監聽 `StatusEvent.NOTF_VIEW_READY` 事件且檢視器由Experience Manager提供服務，則完整事件型別為 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，則事件接聽程式程式碼會如下所示：

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
```
