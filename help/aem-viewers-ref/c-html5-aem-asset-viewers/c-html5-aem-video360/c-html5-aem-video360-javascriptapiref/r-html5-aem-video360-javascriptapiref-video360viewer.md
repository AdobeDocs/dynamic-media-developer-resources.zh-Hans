---
description: Video360查看器的JavaScript API参考。
seo-description: Video360查看器的JavaScript API参考。
seo-title: Video360Viewer
solution: Experience Manager
title: Video360Viewer
topic: Dynamic media
uuid: b5d5e270-687c-40aa-9de4-c5bc2a7806f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Viewer{#video-viewer}

Video360查看器的JavaScript API参考。

`Video360Viewer([config])`

构造函数，创建一个新的HTML5 Video360查看器实例。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 可选的JSON配置对象允许所有查看器设置传递给构造函数以避免调用单个setter方法。 包含以下属性： </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID(通常为 <span class="codeph"> DIV)，查看器将插入 </span>其中。 调用此方法时，无需创建容器元素。 但是，运行init()时必 <span class="codeph"> 须存在 </span> 容器。 </p> <p>必需. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON对象，其中属性名称是特定于查看器的配置选项或SDK修饰符，且该属性的值是相应的设置值。 </p> <p>必需. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 处理 </span> 函数- <span class="codeph"> {Object} </span> JSON对象，带有查看器事件回调，其中属性名称是支持的查看器事件的名称，属性值是对相应回调的JavaScript函数引用。 </p> <p>可选。 </p> <p>有关查 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 看器事件 </a> 的更多信息，请参阅事件回调。 </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> JSON对象，带有本地化数据。 可选。 </p> <p>有关 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 详细信息，请参阅用户界面 </a> 元素的本地化。 </p> <p>另请参阅 <i>《查看器SDK用户指南</i> 》和示例，以了解有关对象内容的更多信息。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

