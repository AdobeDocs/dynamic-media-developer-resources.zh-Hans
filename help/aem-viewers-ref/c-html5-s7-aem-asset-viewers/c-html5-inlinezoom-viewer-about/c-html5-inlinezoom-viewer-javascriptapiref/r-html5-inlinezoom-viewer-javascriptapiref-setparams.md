---
description: 内联缩放查看器的JavaScript API参考。
seo-description: 内联缩放查看器的JavaScript API参考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 50fde4b0-2fd8-4341-bb2f-b1785f82ebc1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

内联缩放查看器的JavaScript API参考。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 参数</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value参数对，以&amp; <span class="codeph"> 分隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

将一个或多个参数设置为给定值。 方法参数语法与URL查询字符串相同。 即，它表示与分隔的name=value对 `&`。 与查询字符串中一样，名称和值使用UTF8进行百分比编码。 在调用之 `init()`前，必须调用此参数。 如果将查看器配置信息与 `config` JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

