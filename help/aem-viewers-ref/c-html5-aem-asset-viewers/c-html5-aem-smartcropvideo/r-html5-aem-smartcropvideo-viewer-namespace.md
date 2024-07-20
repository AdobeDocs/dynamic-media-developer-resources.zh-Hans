---
title: Viewer SDK命名空间
description: Viewer SDK命名空间
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Viewer SDK命名空间{#viewer-sdk-namespace}

查看器由许多Viewer SDK组件构建。 通常，网页不需要直接与SDK组件API交互；查看器API本身涵盖了所有常见需求。

但是，一些高级用例要求网页使用`getComponent()`查看器API引用内部SDK组件，然后使用SDK本身API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器运行的环境。 如果查看器在Adobe Experience Manager中运行，查看器会将SDK组件加载到`s7viewers.s7sdk`命名空间中。 同样，Dynamic Media Classic提供的查看器将SDK加载到`s7classic.s7sdk`中。

在任一情况下，查看器中的SDK使用的命名空间都将`s7viewers`或`s7classic`作为前缀。 此外，它与SDK用户指南或SDK API文档中使用的纯`s7sdk`命名空间不同。 因此，在编写与内部查看器组件通信的自定义应用程序代码时，必须使用完全限定的SDK命名空间。

例如，如果您计划侦听`StatusEvent.NOTF_VIEW_READY`事件并且从Experience Manager提供查看器，则完全限定的事件类型为`s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，事件侦听器代码将类似于以下内容：

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
