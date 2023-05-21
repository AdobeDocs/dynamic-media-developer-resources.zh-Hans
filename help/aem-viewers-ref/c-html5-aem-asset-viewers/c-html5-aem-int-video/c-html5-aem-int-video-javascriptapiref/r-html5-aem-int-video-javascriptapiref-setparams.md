---
title: setParams
description: 互動式視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 32d26999-7815-4c71-ad4c-b7db99ec3d3b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setParams{#setparams}

互動式視訊檢視器的JavaScript API參考。

` setParams( *`引數`*)`

將一或多個引數設定為指定值。 方法引數語法與URL查詢字串相同。 也就是說，它代表名稱=值配對，以分隔 `&`. 如同查詢字串，名稱和值會使用UTF8進行百分比編碼。 呼叫之前 `init()`，則必須呼叫此引數。

如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用： `config` 建構函式的JSON物件。

另請參閱 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


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
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
