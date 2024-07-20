---
title: setParam
description: 适用于混合媒体查看器的JavaScript API参考。
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

适用于混合媒体查看器的JavaScript API参考。

` setParam( *`名称，值`*)`

将查看器参数设置为指定的值。 参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数在`init()`之前调用。 如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名称</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>参数名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>参数值。 值不能采用百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
