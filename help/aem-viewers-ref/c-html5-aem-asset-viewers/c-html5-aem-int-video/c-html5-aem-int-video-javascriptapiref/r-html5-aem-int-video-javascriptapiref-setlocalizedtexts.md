---
description: 交互式视频查看器的JavaScript API参考。
seo-description: 交互式视频查看器的JavaScript API参考。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic Media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

交互式视频查看器的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

为一个或多个区域设置本地化符号值。 必须在`init()`之前调用此参数。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph">对象</span>}个JSON对象，含本地化数据。 </p> <p>有关详细信息，请参见<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">用户界面元素</a>的本地化。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

