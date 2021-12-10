---
title: setParams
description: 视频查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: af31b5eb-2051-4f4c-861d-67ada3248fd6
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---

# setParams{#setparams}

视频查看器的JavaScript API引用。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value参数对，分隔为 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

将一个或多个参数设置为给定值。 方法参数语法与URL查询字符串相同。 即，它表示与 `&`. 与查询字符串一样，名称和值使用UTF8进行百分比编码。 在调用之前 `init()`，则必须调用此参数。

如果查看器配置信息是通过 `config` 将JSON对象转换为构造函数。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
