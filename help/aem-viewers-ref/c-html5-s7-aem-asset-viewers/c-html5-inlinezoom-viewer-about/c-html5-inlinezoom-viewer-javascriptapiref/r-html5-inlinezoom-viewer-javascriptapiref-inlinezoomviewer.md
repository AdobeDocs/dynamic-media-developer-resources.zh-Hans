---
description: 内联缩放查看器的JavaScript API参考。
seo-description: 内联缩放查看器的JavaScript API参考。
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
topic: Dynamic media
uuid: 23617eda-f4c9-4908-9f63-593849c12fc7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutViewer{#flyoutviewer}

内联缩放查看器的JavaScript API参考。

`FlyoutViewer([config])`

构造函数；创建新的内联缩放查看器实例。

## 参数 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 可选JSON配置对象允许所有查看器设置传递给构造函数，并避免调用单个setter方法。 包含以下属性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID(通常为 <span class="codeph"> DIV)，查看器 </span>将插入该DOM容器。 无需在调用此方法之前创建容器元素。 但是，运行init()时必 <span class="codeph"> 须存在 </span> 容器。 必需. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON对象，其中属性名称是特定于查看器的配置选项或SDK修饰符，而该属性的值是相应的设置值。 必需. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 处理 </span> 函数- <span class="codeph"> {Object} </span> JSON对象(带有查看器事件回调)，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 可选。 <p>有关查 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> 看器事件 </a> 的更多信息，请参阅事件回调。 </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedText </span> - { <span class="codeph"> Object </span>} JSON对象(含本地化数据)。 可选。 </p> <p>有关 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> 详细信息，请参阅用户界面 </a> 元素的本地化。 </p> <p>有关对 <i>象内容的详细信息</i> ，请参阅《查看器SDK用户指南》和示例。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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

