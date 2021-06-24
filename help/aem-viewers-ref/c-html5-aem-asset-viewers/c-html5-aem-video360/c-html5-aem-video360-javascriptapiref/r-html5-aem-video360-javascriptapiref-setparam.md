---
description: Video360查看器的JavaScript API引用。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,Business Practitioner
exl-id: eb739d2d-7512-49e2-be13-10f05e2fcc1e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setParam{#setparam}

Video360查看器的JavaScript API引用。

` setParam( *`name， value`*)`

将查看器参数设置为指定值。 参数是特定于查看器的配置选项或软件开发包修饰符。 此参数在`init()`之前调用。

如果查看器配置信息是与`config` JSON对象一起传递到构造函数的，则此方法是可选的。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 参数 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}参 </span> 数的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 参数的{ </span> string}值。该值不能进行百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
