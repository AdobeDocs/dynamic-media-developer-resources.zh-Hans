---
description: 轮播查看器的JavaScript API引用。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,Business Practitioner
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

轮播查看器的JavaScript API引用。

` setLocalizedTexts( *`localizationInfo`*)`

设置一个或多个区域设置的本地化符号值。 必须在`init()`之前调用此参数。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph">对象</span>}个包含本地化数据的JSON对象。 </p> <p>有关更多信息，请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local">用户界面元素的本地化</a> 。 </p> <p>另请参阅<i>查看器SDK用户指南</i>和示例，以了解有关对象内容的更多信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
