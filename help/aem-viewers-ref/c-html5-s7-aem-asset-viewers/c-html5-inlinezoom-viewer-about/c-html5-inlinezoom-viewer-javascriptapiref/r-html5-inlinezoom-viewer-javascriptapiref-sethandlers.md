---
description: 内联缩放查看器的JavaScript API参考。
seo-description: 内联缩放查看器的JavaScript API参考。
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic Media
uuid: 357b0e33-befa-4b89-add5-67cc9e7fd9e7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---


# setHandlers{#sethandlers}

内联缩放查看器的JavaScript API参考。

`setHandlers(handlers)`

指定零个或多个回调处理函数。 对此方法的调用将完全覆盖之前为该查看器实例分配的事件处理函数。 必须在`init()`之前调用。

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 处理程序  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 具有查看 </span> 器事件回调的{Object} JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local">事件回调</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

