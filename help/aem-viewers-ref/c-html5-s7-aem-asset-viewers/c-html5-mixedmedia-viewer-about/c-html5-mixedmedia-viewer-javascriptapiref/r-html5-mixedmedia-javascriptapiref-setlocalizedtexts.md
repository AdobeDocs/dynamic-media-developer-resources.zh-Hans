---
title: setLocalizedTexts
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 19bc61be-4321-434a-ae2c-4576c7799c0a
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

混合媒體檢視器的JavaScript API參考。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> 物件</span>} JSON物件包含本地化資料。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 使用者介面元素的本地化</a> 以取得詳細資訊。 </p> <p>另請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一或多個地區設定的本地化SYMBOL值。 必須在之前呼叫此引數 `init()`.

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
