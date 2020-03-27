---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 4929884e-b072-4177-83c3-1f9b4e5df569
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setParams{#setparams}

eCatalog Viewer的JavaScript API参考。

[!DNL ` setParams( *`params`*)`]

将一个或多个参数设置为给定值。 方法参数语法与URL查询字符串相同。 即，它表示与分隔的name=value对 [!DNL `&`]。 就像在查询字符串中一样，名称和值使用UTF8以百分比编码。 在调用之 [!DNL `init()`]前，必须调用此参数。

如果查看器配置信息与 [!DNL `config`] JSON对象一起传递到构造函数，则此方法是可选的。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 参数</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value参数对，以&amp; <span class="codeph"> 分隔</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```

