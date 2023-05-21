---
title: setParams
description: 影片影像檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a09e3bc-e79c-4206-be42-0c6ae3d91590
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# setParams{#setparams}

影片影像檢視器的JavaScript API參考。

` setParams( *`引數`*)`

將一或多個引數設定為指定值。 方法引數語法與URL查詢字串相同。 也就是說，它代表名稱=值配對，以分隔 `&`. 在查詢字串中，名稱和值使用UTF8進行百分比編碼。 呼叫之前 `init()`，則必須呼叫此引數。

如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用： `config` 建構函式的JSON物件。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 参数 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 引數</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value引數配對，以分隔 <span class="codeph"> 和</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.fmt=png&ZoomView.iscommand=op_sharpen%3d1")
```
