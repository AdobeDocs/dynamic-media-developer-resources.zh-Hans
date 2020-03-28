---
description: 交互式视频查看器的JavaScript API参考。
seo-description: 交互式视频查看器的JavaScript API参考。
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setLocalizedText{#setlocalizedtexts}

交互式视频查看器的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

为一个或多个区域设置本地化SYMBOL值。 此参数必须在之前调用 `init()`。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 本 <span class="varname"> 地化信 </span> 息 </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON对象(含本地化数据)。 </p> <p>有关 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 详细信息，请参阅用户界面 </a> 元素的本地化。 </p> <p>另请参阅 <i>《查看器SDK用户指南</i> 》和示例，以了解有关对象内容的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另请参阅 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

