---
description: 基本缩放查看器的JavaScript API参考。
seo-description: 基本缩放查看器的JavaScript API参考。
seo-title: BasicZoomViewer
solution: Experience Manager
title: BasicZoomViewer
topic: Dynamic Media
uuid: 727e38af-636a-4eb3-b373-6940169d006b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---


# BasicZoomViewer{#basiczoomviewer}

基本缩放查看器的JavaScript API参考。

`BasicZoomViewer([config])`

构造函数，创建新的基本缩放查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}可 </span> 选的JSON配置对象允许所有查看器设置传递给构造函数，以避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> 容器 </span> ID -  <span class="codeph"> {String}  </span> ID,DOM容器(通常 <span class="codeph"> 是DIV </span>)中插入查看器。调用此方法时，无需创建容器元素。 但是，运行<span class="codeph"> init()</span>时，容器必须存在。 必需. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 参 </span> 数-  <span class="codeph"> {Object} JSON对 </span> 象和查看器配置参数，其中属性名称是特定于查看器的配置选项或SDK修饰符，并且该属性的值是相应的设置值。必需. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 处理 </span> 函数-  <span class="codeph"> {Object} JSON对 </span> 象(带有查看器事件回调)，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。可选。 </p> <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local">事件回调</a>。 </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object} JSON对 </span> 象，带有本地化数据。可选。 </p> <p>有关详细信息，请参见<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">用户界面元素</a>的本地化。 </p> <p> 另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 可选 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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

