---
title: setHandlers
description: 交互式视频查看器的JavaScript API参考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ece8d2ba-30ef-4616-81a6-6028e5f3c66f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandlers{#sethandlers}

交互式视频查看器的JavaScript API参考

`setHandlers(handlers)`

指定零个或多个回调处理程序。 对此方法的调用将完全覆盖以前为该查看器实例分配的事件处理程序。 必须在`init()`之前调用。

## 参数 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">处理程序</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span>具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">事件回调</a>。 </p> </td> 
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
