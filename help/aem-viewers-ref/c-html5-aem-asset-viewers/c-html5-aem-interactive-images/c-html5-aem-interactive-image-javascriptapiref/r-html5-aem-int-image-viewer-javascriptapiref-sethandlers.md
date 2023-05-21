---
title: setHandlers
description: 互動式影像檢視器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: a5e42842-dc88-454b-8229-33a65c01bf88
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

互動式影像檢視器的JavaScript API參考

`setHandlers(handlers)`

指定零個或多個回呼處理常式。 對此方法的呼叫會完全覆寫先前為該檢視器執行個體指派的事件處理常式。 必須在以下時間之前呼叫： `init()`.

## 参数 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 處理常式 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 具有檢視器事件回撥的JSON物件。 屬性名稱是支援的檢視器事件的名稱。 屬性值是對適當回呼的JavaScript函式參考。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </td> 
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
