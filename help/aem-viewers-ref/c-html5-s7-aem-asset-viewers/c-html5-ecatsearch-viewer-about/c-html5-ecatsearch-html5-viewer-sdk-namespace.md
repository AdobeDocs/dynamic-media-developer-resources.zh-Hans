---
description: 查看器SDK命名空间
solution: Experience Manager
title: 查看器SDK命名空间
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
TQID: 'https://experienceleague.adobe.com/wS6VG2Eo73QO7-kbRLVCZ-DOrSWUb6XOB92J-zP7QV8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# 查看器SDK命名空间{#viewer-sdk-namespace}

查看器由多个Viewer SDK组件构建。 在大多数情况下，网页不需要直接与SDK组件API交互；查看器API本身涵盖了所有常见需求。

但是，一些高级用例要求网页使用`getComponent()`查看器API获取对内部SDK组件的引用，然后使用SDK本身API的所有灵活性。

查看器用于加载和初始化SDK组件的命名空间取决于查看器运行的环境。 如果查看器在AEM (Adobe Experience Manager)中运行，查看器会将SDK组件加载到`s7viewers.s7sdk`命名空间中。 Dynamic Media Classic提供的查看器将SDK加载到`s7classic.s7sdk`中。

在任一情况下，查看器内SDK使用的命名空间都将`s7viewers`或`s7classic`作为前缀。 此外，它与《SDK用户指南》或SDK API文档中使用的纯`s7sdk`命名空间不同。

因此，在编写与内部查看器组件通信的自定义应用程序代码时，使用完全限定的SDK命名空间很重要。

例如，如果您计划侦听`StatusEvent.NOTF_VIEW_READY`事件，并且查看器来自Dynamic Media Classic，则完全限定的事件类型为`s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`，事件侦听器代码将类似于以下内容：

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

