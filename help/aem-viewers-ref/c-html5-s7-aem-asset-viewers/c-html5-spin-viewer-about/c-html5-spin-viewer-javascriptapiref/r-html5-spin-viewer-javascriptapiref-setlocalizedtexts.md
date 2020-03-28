---
description: Spin Viewer的JavaScript API参考。
seo-description: Spin Viewer的JavaScript API参考。
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: bf136479-8ac8-4151-8911-377eed631aa2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedText{#setlocalizedtexts}

Spin Viewer的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 本 <span class="varname"> 地化信息</span></span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON对象(含本地化数据)。 </p> <p>有关 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> 详细信息，请参阅用户界面元素的本地化</a> 。 </p> <p>另请参阅 <i>《查看器SDK用户指南</i> 》和示例，以了解有关对象内容的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

为一个或多个区域设置本地化SYMBOL值。 此参数必须在之前调用 `init()`。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

