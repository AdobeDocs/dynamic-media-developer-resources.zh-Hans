---
description: 查看器SDK命名空间
solution: Experience Manager
title: 查看器SDK命名空间
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# 查看器SDK命名空间{#viewer-sdk-namespace}

查看器由许多查看器SDK组件构建。 在大多数情况下，网页无需与SDK组件API直接交互；查看器API本身涵盖了所有常见需求。

但是，某些高级用例要求网页使用`getComponent()`查看器API获取对内部SDK组件的引用，然后使用SDK自身API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器操作的环境。 如果查看器在AEM(Adobe Experience Manager)中运行，则查看器将SDK组件加载到`s7viewers.s7sdk`命名空间中。 从Dynamic Media Classic提供的查看器将SDK加载到`s7classic.s7sdk`中。

在任一情况下，查看器中的SDK所使用的命名空间以`s7viewers`或`s7classic`作为前缀。 而且，它与《SDK用户指南》或SDK API文档中使用的纯`s7sdk`命名空间不同。

因此，在编写与内部查看器组件通信的自定义应用程序代码时，务必使用完全限定的SDK命名空间。

例如，如果您计划侦听`StatusEvent.NOTF_VIEW_READY`事件，并且查看器从Dynamic Media Classic提供，则完全限定的事件类型为`s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，而事件侦听器代码类似于以下内容：

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

