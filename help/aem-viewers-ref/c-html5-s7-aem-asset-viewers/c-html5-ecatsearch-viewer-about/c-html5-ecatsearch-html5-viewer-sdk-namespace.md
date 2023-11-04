---
description: Viewer SDK命名空间
solution: Experience Manager
title: Viewer SDK命名空间
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Viewer SDK命名空间{#viewer-sdk-namespace}

查看器由许多Viewer SDK组件构建。 在大多数情况下，网页不需要直接与SDK组件API交互；查看器API本身涵盖了所有常见需求。

但是，一些高级用例要求网页使用获取对内部SDK组件的引用 `getComponent()` 查看器API，然后使用SDK本身API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器运行的环境。 如果查看器在AEM (Adobe Experience Manager)中运行，查看器会将SDK组件加载到 `s7viewers.s7sdk` 命名空间。 Dynamic Media Classic提供的查看器会将SDK加载到 `s7classic.s7sdk`.

在任一情况下，查看器中的SDK使用的命名空间具有 `s7viewers` 或 `s7classic` 作为前缀。 而且这和普通人不一样 `s7sdk` SDK用户指南或SDK API文档中使用的命名空间。

因此，在编写与内部查看器组件通信的自定义应用程序代码时，使用完全限定的SDK命名空间很重要。

例如，如果您计划侦听 `StatusEvent.NOTF_VIEW_READY` 事件且查看器来自Dynamic Media Classic，完全限定的事件类型为 `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，则事件侦听器代码类似于以下内容：

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
