---
description: 轮播查看器的JavaScript API引用。
solution: Experience Manager
title: 轮播查看器
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 轮播查看器{#carouselviewer}

轮播查看器的JavaScript API引用。

`CarouselViewer([config])`

构造函数，创建一个新的HTML 5轮播查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}可选 </span> 的JSON配置对象，允许将所有查看器设置传递到构造函数，以避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String} </span>  DOM容器(通常是 <span class="codeph"> DIV </span>)的ID，查看器将插入其中。调用此方法时，无需创建容器元素。 但是，运行<span class="codeph"> init()</span>时，容器必须存在。 </p> <p>必需. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 参数 </span>  -  <span class="codeph"> {Object}  </span> JSON对象，其中属性名称是特定于查看器的配置选项或SDK修饰符，并且该属性的值是相应的设置值。 </p> <p>必需. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 处理 </span> 程序 —  <span class="codeph"> {Object} </span> 具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>可选。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">事件回调</a> ，以了解有关查看器事件的更多信息。 </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> </p> <p> 包含本地化数据的JSON对象。 有关对象内容的更多信息，请参阅用户界面元素的本地化和示例。 </p> <p>可选 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
