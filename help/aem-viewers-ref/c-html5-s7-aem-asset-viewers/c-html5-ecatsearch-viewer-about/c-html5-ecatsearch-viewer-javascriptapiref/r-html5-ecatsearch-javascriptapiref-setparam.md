---
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0dd57c7e-c20f-4e8f-a872-42e24305fc0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

eCatalog檢視器的JavaScript API參考。

[!DNL ` setParam( *`名稱，值`*)`]

將檢視器引數設定為指定的值。 引數是檢視器特定的組態選項或軟體開發套件修飾元。 此引數是在以下時間之前呼叫： [!DNL `init()`].

如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用： [!DNL `config`] 建構函式的JSON物件。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 引數名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 引數值。 值不得以百分比編碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
[!DNL <instance>.setParam("style", "customStyle.css")]
```
