---
description: Video360查看器的JavaScript API参考。
seo-description: Video360查看器的JavaScript API参考。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: c8c40e88-530f-4af8-be9a-2e88addd6907
translation-type: tm+mt
source-git-commit: 9abcdc9a45a19ea9c761eef6aef68abac33b9655

---


# setParam{#setparam}

Video360查看器的JavaScript API参考。

` setParam( *`name, value`*)`

将查看器参数设置为指定值。 该参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数之前被调用 `init()`。

如果查看器配置信息是与 `config` JSON对象一起传递到构造函数的，则此方法是可选的。

另请参阅 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 参数 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

