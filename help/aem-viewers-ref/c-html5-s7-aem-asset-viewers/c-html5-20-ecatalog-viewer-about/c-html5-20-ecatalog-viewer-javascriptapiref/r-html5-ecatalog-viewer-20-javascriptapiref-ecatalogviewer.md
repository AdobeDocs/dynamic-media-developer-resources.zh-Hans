---
title: eCatalogViewer
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# eCatalogViewer{#ecatalogviewer}

eCatalog檢視器的JavaScript API參考。

`eCatalogViewer([config])`

建構函式，建立eCatalog檢視器例項。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 設定 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 選用的JSON設定物件，可讓所有檢視器設定傳遞至建構函式，並避免呼叫個別setter方法。 包含以下屬性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM容器的ID (通常是 <span class="codeph"> DIV </span>)，即可將檢視器插入其中。 不需要在呼叫此方法時建立容器元素。 不過，容器必須存在於 <span class="codeph"> init() </span> 執行前填入。 必需. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> 引數 </span> - <span class="codeph"> {Object} </span> 具有檢視器組態引數的JSON物件，其中屬性名稱是檢視器特定的組態選項或SDK修飾元，而該屬性的值是對應的設定值。 必需. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 處理常式 </span> - <span class="codeph"> {Object} </span> 具有檢視器事件回呼的JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是對適當回呼的JavaScript函式參照。 可选. </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 事件回呼 </a> 以取得檢視器事件的詳細資訊。 </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedText </span> - { <span class="codeph"> 物件 </span>} JSON物件包含本地化資料。 可选. </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 使用者介面元素的本地化 </a> 以取得詳細資訊。 </p> <p>另請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
