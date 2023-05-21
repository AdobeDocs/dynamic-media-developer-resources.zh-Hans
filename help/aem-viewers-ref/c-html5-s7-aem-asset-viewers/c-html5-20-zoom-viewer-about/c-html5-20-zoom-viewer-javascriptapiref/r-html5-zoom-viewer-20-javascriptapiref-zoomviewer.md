---
title: 縮放檢視器
description: 縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---

# 縮放檢視器{#zoomviewer}

縮放檢視器的JavaScript API參考。

`ZoomViewer([config])`

建構函式，建立縮放檢視器例項。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 選用的JSON設定物件，可讓所有檢視器設定傳遞至建構函式，以避免呼叫個別setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM容器的ID (通常是 <span class="codeph"> DIV </span>)，即可將檢視器插入其中。 呼叫此方法時，不需要建立容器元素。 不過，容器必須存在於 <span class="codeph"> init() </span> 執行前填入。 必需. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> 引數 </span> - <span class="codeph"> {Object} </span> 具有檢視器組態引數的JSON物件，其中屬性名稱為檢視器特定的組態選項或SDK修飾元，且該屬性的值為對應的設定值。 必需. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> 處理常式 </span> - <span class="codeph"> {Object} </span> 具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是對適當回呼的JavaScript函式參考。 可选. <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> 含有本地化資料的JSON物件。 可选. <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 使用者介面元素的本地化 </a> 以取得詳細資訊。 </p> <p>另請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
