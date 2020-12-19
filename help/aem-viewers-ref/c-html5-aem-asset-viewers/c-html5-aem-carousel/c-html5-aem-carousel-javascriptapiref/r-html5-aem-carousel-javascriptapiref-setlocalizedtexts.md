---
description: 旋转式查看器的JavaScript API参考。
seo-description: 旋转式查看器的JavaScript API参考。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

旋转式查看器的JavaScript API参考。

` setLocalizedTexts( *`localizationInfo`*)`

为一个或多个区域设置本地化符号值。 必须在`init()`之前调用此参数。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON对象，含本地化数据。 </p> <p>有关详细信息，请参见<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local">用户界面元素本地化</a>。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

