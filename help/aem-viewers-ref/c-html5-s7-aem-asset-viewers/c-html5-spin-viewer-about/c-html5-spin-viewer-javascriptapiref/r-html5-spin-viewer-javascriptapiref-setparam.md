---
description: Spin Viewer的JavaScript API参考。
seo-description: Spin Viewer的JavaScript API参考。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 5f7be1d4-28aa-497c-9067-853c227aa11a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Spin Viewer的JavaScript API参考。

` setParam( *`name, value`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名称 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数的值。 该值不能以百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

将查看器参数设置为指定值。 该参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数之前被调用 `init()`。

如果查看器配置信息与 `config` JSON对象一起传递到构造函数，则此方法是可选的。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

