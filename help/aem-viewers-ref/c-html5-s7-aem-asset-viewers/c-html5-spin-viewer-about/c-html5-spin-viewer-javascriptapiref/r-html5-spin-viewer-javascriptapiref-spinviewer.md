---
title: 旋转查看器
description: 旋转查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# 旋转查看器{#spinviewer}

旋转查看器的JavaScript API参考。

`SpinViewer([config])`

构造函数，创建新的旋转查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">配置</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span>可选JSON配置对象，允许所有查看器设置传递到构造函数，并避免调用单个setter方法。 包含以下属性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> 查看器插入的DOM容器的<span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID（通常为<span class="codeph"> DIV </span>）。 在调用此方法时，无需创建容器元素。 但是，运行<span class="codeph"> init() </span>时容器必须存在。 必需. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph">参数</span> - <span class="codeph"> {Object} </span> JSON对象具有查看器配置参数，其中属性名称是查看器特定的配置选项或SDK修饰符，并且该属性的值是相应的设置值。 必需. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph">处理程序</span> - <span class="codeph"> {Object} </span>具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 可选. </p> <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local">事件回调</a>。 </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON对象包含本地化数据。 可选. </p> <p>有关详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local">用户界面元素</a>的本地化。 </p> <p>另请参阅<i>Viewer SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
