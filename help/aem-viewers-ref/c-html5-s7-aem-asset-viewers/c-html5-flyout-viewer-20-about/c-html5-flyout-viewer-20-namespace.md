---
title: Viewer SDK命名空间
description: Viewer SDK命名空间
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 06a7110a-3a6f-42f9-b729-e8f96762c64e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Viewer SDK命名空间{#viewer-sdk-namespace}

查看器由多个Viewer SDK组件构建。 通常，网页无需直接与SDK组件API交互；查看器API本身涵盖了所有常见需求。

但是，一些高级用例要求网页使用引用内部SDK组件 `getComponent()` 查看器API，然后使用SDK本身的API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器运行的环境。 如果查看器在Adobe Experience Manager中运行，则查看器会将SDK组件加载到 `s7viewers.s7sdk` 命名空间。 同样，Dynamic Media Classic提供的查看器会将SDK加载到 `s7classic.s7sdk`.

在任一情况下，SDK在查看器中使用的命名空间具有以下任一功能 `s7viewers` 或 `s7classic` 作为前缀。 它和普通人不一样 `s7sdk` SDK用户指南或SDK API文档中使用的命名空间。 因此，在编写与内部查看器组件通信的自定义应用程序代码时，必须使用完全限定的SDK命名空间。

例如，如果您计划侦听 `StatusEvent.NOTF_VIEW_READY` 事件和从Experience Manager提供查看器的情况下，完全限定的事件类型为 `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，则事件侦听器代码类似于以下内容：

```html {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
