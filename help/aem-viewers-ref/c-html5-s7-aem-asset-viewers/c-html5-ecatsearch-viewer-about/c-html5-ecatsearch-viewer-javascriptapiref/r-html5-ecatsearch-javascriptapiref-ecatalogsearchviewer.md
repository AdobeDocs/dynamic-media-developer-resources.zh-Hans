---
description: eCatalog SearchViewer的JavaScript API引用。
solution: Experience Manager
title: eCatalogSearchViewer
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: a7289d23-b2f6-4730-99fa-331174968e05
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# eCatalogSearchViewer{#ecatalogsearchviewer}

eCatalog SearchViewer的JavaScript API引用。

[!DNL `eCatalogSearchViewer([config])`]

构造函数，创建一个新的eCatalog搜索查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}可选 </span> 的JSON配置对象，允许将所有查看器设置传递到构造函数，并避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String} </span>  DOM容器(通常是 <span class="codeph"> DIV </span>)的ID，查看器将插入其中。无需在调用此方法之前创建容器元素。 但是，运行<span class="codeph"> init()</span>时，容器必须存在。 必需. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> 参数 </span>  -  <span class="codeph"> {Object}  </span> JSON对象，其中属性名称是特定于查看器的配置选项或SDK修饰符，并且该属性的值是相应的设置值。必需. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 处理 </span> 程序 —  <span class="codeph"> {Object} </span> 具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。可选。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local">事件回调</a> ，以了解有关查看器事件的更多信息。 </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts  </span>  — 包含本 <span class="codeph"> 地化 </span>数据的{对象} JSON对象。可选。 </p> <p>有关更多信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">用户界面元素的本地化</a> 。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
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
