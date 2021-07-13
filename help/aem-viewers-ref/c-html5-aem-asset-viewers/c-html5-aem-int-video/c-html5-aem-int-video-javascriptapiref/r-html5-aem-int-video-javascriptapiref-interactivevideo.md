---
description: 交互式视频查看器的JavaScript API引用。
solution: Experience Manager
title: InteractiveVideoViewer
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# InteractiveVideoViewer{#interactivevideoviewer}

交互式视频查看器的JavaScript API引用。

`InteractiveVideoViewer([config])`

构造函数，创建一个新的交互式视频查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}可选 </span> 的JSON配置对象，允许将所有查看器设置传递到构造函数，以避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> DOM容器的ID(通常是 <span class="codeph"> DIV </span>)，查看器将插入其中。调用此方法时，无需创建容器元素。 但是，运行<span class="codeph"> init()</span>时，容器必须存在。 </p> <p>必需. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 参数 </span>  -  <span class="codeph"> {Object}  </span> JSON对象，其中属性名称是特定于查看器的配置选项或SDK修饰符，并且该属性的值是相应的设置值。 </p> <p>必需. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 处理 </span> 程序 —  <span class="codeph"> {Object} </span> 具有查看器事件回调的JSON对象，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>可选。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">事件回调</a> ，以了解有关查看器事件的更多信息。 </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedText -  </span> {Object} <span class="codeph"> 具有本 </span> 地化数据的JSON对象。可选。 </p> <p>有关更多信息，请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">用户界面元素的本地化</a> 。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
