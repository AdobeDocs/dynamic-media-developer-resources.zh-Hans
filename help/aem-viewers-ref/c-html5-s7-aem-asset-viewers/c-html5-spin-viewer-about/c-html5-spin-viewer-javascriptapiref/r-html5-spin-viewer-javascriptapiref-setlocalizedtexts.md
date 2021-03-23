---
description: 旋转查看器的JavaScript API参考。
seo-description: 旋转查看器的JavaScript API参考。
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
uuid: bf136479-8ac8-4151-8911-377eed631aa2
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

旋转查看器的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>}包含本地化数据的JSON对象。 </p> <p>有关详细信息，请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local">用户界面元素本地化</a>。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的详细信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

为一个或多个区域设置本地化SYMBOL值。 必须在`init()`之前调用此参数。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

