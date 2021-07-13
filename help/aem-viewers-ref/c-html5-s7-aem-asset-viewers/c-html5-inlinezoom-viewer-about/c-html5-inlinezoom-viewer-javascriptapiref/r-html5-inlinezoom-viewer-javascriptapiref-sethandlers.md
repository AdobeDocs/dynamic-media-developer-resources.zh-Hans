---
description: 内联缩放查看器的JavaScript API引用。
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,User
exl-id: 233fadf5-4b09-406d-959b-c2c9c4524021
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# setHandlers{#sethandlers}

内联缩放查看器的JavaScript API引用。

`setHandlers(handlers)`

指定零个或多个回调处理程序。 对此方法的调用将完全覆盖之前为该查看器实例分配的事件处理程序。 必须在`init()`之前调用。

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 处理程序  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 具有查看 </span> 器事件回调的{Object} JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local">事件回调</a> ，以了解有关查看器事件的更多信息。 </p> </td> 
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
