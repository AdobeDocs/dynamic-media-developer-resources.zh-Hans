---
title: 全景查看器
description: 构造函数，创建新的HTML5轮盘式查看器实例。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 全景查看器{#panoramicviewer}

`PanoramicViewer([config])`
构造函数，创建新的HTML5全景查看器实例。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

配置{Object}可选JSON配置对象，允许将所有查看器设置传递到构造函数，并避免调用单个setter方法。 包含以下属性：
* containerId - {String} DOM容器的ID（通常是DIV），查看器插入到该容器中。 不必在调用此方法时创建容器元素，但是在执行init()时容器必须存在。 必需
* params - {Object} JSON对象，带有查看器配置参数，其中属性名称是查看器特定的配置选项或SDK修饰符，并且该属性的值是相应的设置值。 必需
* 处理程序 — 具有查看器事件回调的{Object} JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 有关查看器事件的更多信息，请参阅事件回调部分。 可选


## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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
