---
description: Video Viewer的JavaScript API参考。
seo-description: Video Viewer的JavaScript API参考。
seo-title: VideoViewer
solution: Experience Manager
title: VideoViewer
uuid: ad180d92-3e5c-4ded-b82b-79c23aa5c597
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# VideoViewer{#videoviewer}

Video Viewer的JavaScript API参考。

`VideoViewer([config])`

构造函数；创建新的Video Viewer实例。

## 参数 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}可 </span> 选的JSON配置对象允许所有查看器设置传递给构造函数，并避免调用单个setter方法。包含以下属性： </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID（通常是DIV），查 <span class="codeph"> 看 </span>器将插入该DOM容器。调用此方法时不必创建容器元素。 但是，运行<span class="codeph"> init()</span>时必须存在容器。 必需. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params -  </span> { <span class="codeph"> Object} JSON对象，其中 </span> 属性名称是特定于查看器的配置选项或SDK修饰符，而该属性的值是相应的设置值。必需. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 处理 </span> 函数 —  <span class="codeph"> {Object} JSON对 </span> 象(带有查看器事件回调)，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。可选。 <p>有关查看器事件的详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local">事件回调</a>。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object </span>} JSON对象(包含本地化数据)。可选。 </p> <p>有关详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local">查看器SDK命名空间</a>。 </p> <p>有关对象内容的详细信息，请参阅<i>查看器SDK用户指南</i>和示例。 可选。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

