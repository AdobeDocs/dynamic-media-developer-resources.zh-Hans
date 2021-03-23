---
description: Carousel Viewer的JavaScript API参考。
seo-description: Carousel Viewer的JavaScript API参考。
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: 87f16ea9-0267-4114-9aeb-a68fdb616a88
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---


# setParam{#setparam}

Carousel Viewer的JavaScript API参考。

` setParam( *`name， value`*)`

将查看器参数设置为指定值。 该参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数在`init()`之前调用。

如果将查看器配置信息与`config` JSON对象一起传递到构造函数，则此方法是可选的。

另请参阅[xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md)。

## 参数 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名称  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}参 </span> 数的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数值。该值不能以百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```

