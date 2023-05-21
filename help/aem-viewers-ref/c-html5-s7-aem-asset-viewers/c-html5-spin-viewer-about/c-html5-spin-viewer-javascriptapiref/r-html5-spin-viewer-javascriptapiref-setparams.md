---
title: setParams
description: 迴轉檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 61d5b791-12bd-444a-add1-5537c71881fe
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

迴轉檢視器的JavaScript API參考。

` setParams( *`引數`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 引數</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value引數配對，以分隔 <span class="codeph"> 和</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

將一或多個引數設定為指定值。 方法引數語法與URL查詢字串相同。 也就是說，它代表名稱=值配對，以分隔 `&`. 如同查詢字串，名稱和值會使用UTF8進行百分比編碼。 呼叫之前 `init()`，則必須呼叫此引數。

如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用： `config` 建構函式的JSON物件。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("SpinView.zoomstep=2,3&SpinView.iscommand=op_sharpen%3d1")
```
