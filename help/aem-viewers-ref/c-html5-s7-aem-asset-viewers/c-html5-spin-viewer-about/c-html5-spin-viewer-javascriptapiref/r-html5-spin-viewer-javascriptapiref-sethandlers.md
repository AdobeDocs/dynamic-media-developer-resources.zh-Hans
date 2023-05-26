---
title: setHandlers
description: 旋转查看器的JavaScript API参考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: f9e0b93e-fb27-4530-93cf-8246948423d9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

旋转查看器的JavaScript API参考

`setHandlers(handlers)`

指定零个或多个回调处理程序。 对此方法的调用将完全覆盖以前为该查看器实例分配的事件处理程序。 必须在之前调用 `init()`.

## 参数 {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 处理程序 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 具有查看器事件回调的JSON对象，其中属性名称是受支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>参见 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> 事件回调 </a> 以了解有关查看器事件的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
