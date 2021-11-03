---
description: 智能裁剪视频查看器的JavaScript API引用。
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 37d14494-cdb2-45f7-96e2-d7a9e90edad3
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---

# setHandlers{#sethandlers}

智能裁剪视频查看器的JavaScript API引用。

`setHandlers(handlers)`

指定零个或多个回调处理程序。 对此方法的调用将完全覆盖之前为该查看器实例分配的事件处理程序。 必须在 `init()`.

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 处理程序 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {对象} </span> 具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> 事件回调 </a> 以了解有关查看器事件的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
