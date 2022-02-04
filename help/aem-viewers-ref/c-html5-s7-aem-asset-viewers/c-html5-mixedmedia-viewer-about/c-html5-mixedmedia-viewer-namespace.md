---
title: 查看器SDK命名空间
description: 查看器SDK命名空间
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 570f8eee-a7dd-40aa-b732-03f97d2544c0
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 查看器SDK命名空间{#viewer-sdk-namespace}

查看器由许多查看器SDK组件构建。 通常，网页不需要直接与SDK组件API交互；查看器API本身涵盖了所有常见需求。

但是，某些高级用例要求网页使用 `getComponent()` 查看器API，然后使用SDK自身API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器运行的环境。 如果查看器在Adobe Experience Manager中运行，则查看器会将SDK组件加载到 `s7viewers.s7sdk` 命名空间。 同样，Dynamic Media Classic提供的查看器将SDK加载到 `s7classic.s7sdk`.

无论哪种情况，查看器中SDK使用的命名空间都具有以下任一值 `s7viewers` 或 `s7classic` 作为前缀。 这和平原不同 `s7sdk` 《SDK用户指南》或SDK API文档中使用的命名空间。 因此，在编写与内部查看器组件通信的自定义应用程序代码时，务必使用完全限定的SDK命名空间。

例如，如果您打算 `StatusEvent.NOTF_VIEW_READY` 事件，则Experience Manager会提供完全限定的事件类型为 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，且事件侦听器代码类似于以下内容：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
