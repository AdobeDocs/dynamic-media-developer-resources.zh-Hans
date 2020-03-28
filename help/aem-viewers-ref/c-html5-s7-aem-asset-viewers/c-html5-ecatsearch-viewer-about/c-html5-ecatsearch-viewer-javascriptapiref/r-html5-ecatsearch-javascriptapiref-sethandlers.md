---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 602fbf82-429b-443c-9163-f4d2e2b922dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setHandlers{#sethandlers}

eCatalog Viewer的JavaScript API参考。

[!DNL `setHandlers(handlers)`]

指定零个或多个回调处理函数。 对此方法的调用将完全覆盖先前为该查看器实例分配的事件处理函数。 必须在之前调用 `init()`。

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 处理程序 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 具有查看器事件回调的{Object} </span> JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>有关查 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 看器事件 </a> 的更多信息，请参阅事件回调。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

