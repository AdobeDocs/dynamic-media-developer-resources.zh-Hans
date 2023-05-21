---
title: setParam
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 610a5a7d-1314-48bc-a640-319139d64adc
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# setParam{#setparam}

混合媒體檢視器的JavaScript API參考。

` setParam( *`名稱，值`*)`

將檢視器引數設定為指定的值。 引數是檢視器特定的組態選項或軟體開發套件修飾元。 此引數是在以下時間之前呼叫： `init()`. 如果透過以下方式傳遞檢視器設定資訊，則此方法為選用： `config` 建構函式的JSON物件。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

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
<instance>.setParam("style", "customStyle.css")
```
