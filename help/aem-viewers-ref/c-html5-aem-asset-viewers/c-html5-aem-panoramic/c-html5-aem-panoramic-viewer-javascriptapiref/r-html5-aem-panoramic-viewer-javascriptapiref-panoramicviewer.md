---
title: 全景檢視器
description: 建構函式，建立新的HTML5轉盤檢視器例項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 全景檢視器{#panoramicviewer}

`PanoramicViewer([config])`
建構函式，建立新的HTML5全景檢視器例項。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

設定{Object}選用的JSON設定物件，允許將所有檢視器設定傳遞至建構函式，並避免呼叫個別setter方法。 包含以下屬性：
* containerId — 檢視器插入的DOM容器（通常是DIV）的{String} ID。 不需要在呼叫此方法時建立container元素，但是在執行init()時容器必須存在。 必需
* params — 具有檢視器組態引數的{Object} JSON物件，其中屬性名稱為檢視器特定的組態選項或SDK修飾元，且該屬性的值為對應的設定值。 必需
* 處理常式 — 具有檢視器事件回呼的{Object} JSON物件，其中屬性名稱是支援的檢視器事件的名稱，屬性值是對適當回呼的JavaScript函式參考。 如需檢視器事件的詳細資訊，請參閱事件回呼區段。 可选


## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
	"initComplete":function() {
		console.log("init complete");
}
}
});
```
