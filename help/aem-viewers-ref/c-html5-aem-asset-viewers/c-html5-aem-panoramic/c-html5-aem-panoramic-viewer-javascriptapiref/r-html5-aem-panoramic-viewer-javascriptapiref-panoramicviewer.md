---
title: PanoramicViewer
description: 构造函数，创建一个新的HTML5轮播查看器实例。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 13d15bd9483d939de8391d5cfe814c48fed30f22
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
构造函数，创建一个新的HTML5全景查看器实例。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

配置{Object}可选JSON配置对象，允许将所有查看器设置传递给构造函数，并避免调用单个setter方法。 包含以下属性：
* containerId — 将插入查看器的DOM容器（通常为DIV）的{String} ID。 调用此方法时，不必创建容器元素，但执行init()时必须存在容器。 必需
* params - {Object} JSON对象，带有查看器配置参数，其中属性名称是特定于查看器的配置选项或SDK修饰符，并且该属性的值是相应的设置值。 必需
* 处理程序 — 具有查看器事件回调的{Object} JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 有关查看器事件的更多信息，请参阅事件回调一节。 可选


## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
