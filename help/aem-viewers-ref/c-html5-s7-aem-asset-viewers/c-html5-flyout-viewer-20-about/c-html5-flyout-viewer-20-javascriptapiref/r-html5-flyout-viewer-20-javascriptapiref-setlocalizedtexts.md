---
description: Flyout Viewer的JavaScript API参考。
seo-description: Flyout Viewer的JavaScript API参考。
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: 69341735-5ebe-4e3b-acad-b6b916b11bb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedText{#setlocalizedtexts}

Flyout Viewer的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 本 <span class="varname"> 地化信 </span> 息 </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON对象(含本地化数据)。 </p> <p>有关 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> 详细信息，请参阅用户界面 </a> 元素的本地化。 </p> <p>有关对 <i>象内容的详细信息</i> ，请参阅《查看器SDK用户指南》和示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

为一个或多个区域设置本地化SYMBOL值。 此参数必须在之前调用 `init()`。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

