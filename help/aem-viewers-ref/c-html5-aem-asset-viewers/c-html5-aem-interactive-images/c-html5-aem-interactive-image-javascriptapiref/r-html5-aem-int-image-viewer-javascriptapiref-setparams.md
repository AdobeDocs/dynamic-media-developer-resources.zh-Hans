---
title: setParams
description: 视频图像查看器的JavaScript API引用。
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

视频图像查看器的JavaScript API引用。

` setParams( *`params`*)`

将一个或多个参数设置为给定值。 方法参数语法与URL查询字符串相同。 即，它表示与`&`分隔的名称=值对。 在查询字符串中，名称和值使用UTF8进行百分比编码。 在调用`init()`之前，必须调用此参数。

如果查看器配置信息是与`config` JSON对象一起传递到构造函数的，则此方法是可选的。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 参数 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value参数对，以&amp; <span class="codeph"> </span>分隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.fmt=png&ZoomView.iscommand=op_sharpen%3d1")
```
