---
title: setLocalizedTexts
description: 轉盤檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

轉盤檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

設定一或多個地區設定的本地化SYMBOL值。 必須在之前呼叫此引數 `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> 物件</span>} JSON物件包含本地化資料。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> 使用者介面元素的本地化</a> 以取得詳細資訊。 </p> <p>另請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參閱 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
