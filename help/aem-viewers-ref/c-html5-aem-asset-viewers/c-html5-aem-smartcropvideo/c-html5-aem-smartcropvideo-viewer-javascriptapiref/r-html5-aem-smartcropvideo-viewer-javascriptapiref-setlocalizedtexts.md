---
title: setLocalizedTexts
description: setLocalizedTexts
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 313069b6-f114-487a-8322-55b4dff43f68
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# setLocalizedTexts{#setlocalizedtexts}

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> 物件 </span>} JSON物件包含本地化資料。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> 檢視器SDK名稱空間 </a> 以取得詳細資訊。 </p> <p>請參閱 <i>檢視器SDK使用手冊</i> 和範例，以取得物件內容的詳細資訊。 可选. </p> </td> 
  </tr> 
 </tbody> 
</table>

設定一或多個地區設定的本地化SYMBOL值。 必須在之前呼叫此引數 `init()`.

另請參閱 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
