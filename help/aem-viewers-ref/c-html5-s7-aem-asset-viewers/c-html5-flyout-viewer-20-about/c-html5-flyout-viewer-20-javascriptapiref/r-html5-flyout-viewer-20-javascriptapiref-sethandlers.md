---
title: setHandlers
description: 彈出式檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 3a7b2aeb-2de5-4d4c-8974-47b6418140e6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

彈出式檢視器的JavaScript API參考。

`setHandlers(handlers)`

指定零個或多個回呼處理常式。 對此方法的呼叫會完全覆寫先前為該檢視器執行個體指派的事件處理常式。 必須在以下時間之前呼叫： `init()`.

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理常式 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是對適當回呼的JavaScript函式參照。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
