---
title: setHandlers
description: 智慧型裁切視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2f9e0381-650d-4f13-b2ae-8d810c8488f4
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---

# setHandlers{#sethandlers}

智慧型裁切視訊檢視器的JavaScript API參考。

`setHandlers(handlers)`

指定零個或多個回呼處理常式。 對此方法的呼叫會完全覆寫先前為該檢視器執行個體指派的事件處理常式。 必須在以下時間之前呼叫： `init()`.

## 参数 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理常式 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是對適當回呼的JavaScript函式參照。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </td> 
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
