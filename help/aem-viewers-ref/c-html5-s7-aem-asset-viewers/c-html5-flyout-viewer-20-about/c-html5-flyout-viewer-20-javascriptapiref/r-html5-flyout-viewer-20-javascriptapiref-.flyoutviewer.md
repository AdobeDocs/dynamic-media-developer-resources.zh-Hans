---
description: 弹出查看器的JavaScript API参考。
solution: Experience Manager
title: FlyoutViewer
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# FlyoutViewer{#flyoutviewer}

弹出查看器的JavaScript API参考。

`FlyoutViewer([config])`

构造函数；创建新的弹出查看器实例。

## 参数 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}可 </span> 选的JSON配置对象允许所有查看器设置传递给构造函数，并避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID（通常是DIV），查 <span class="codeph"> 看 </span>器将插入该DOM容器。调用此方法时不必创建容器元素。 但是，运行<span class="codeph"> init()</span>时必须存在容器。 必需. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params -  </span> { <span class="codeph"> Object} JSON对象，其中 </span> 属性名称是特定于查看器的配置选项或SDK修饰符，而该属性的值是相应的设置值。必需. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 处理 </span> 函数 —  <span class="codeph"> {Object} JSON对 </span> 象(带有查看器事件回调)，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。可选。 <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local">事件回调</a>。 </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object </span>} JSON对象(包含本地化数据)。可选。 </p> <p>有关详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local">用户界面元素</a>的本地化。 </p> <p>有关对象内容的详细信息，请参阅<i>查看器SDK用户指南</i>和示例。 可选。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
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
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

