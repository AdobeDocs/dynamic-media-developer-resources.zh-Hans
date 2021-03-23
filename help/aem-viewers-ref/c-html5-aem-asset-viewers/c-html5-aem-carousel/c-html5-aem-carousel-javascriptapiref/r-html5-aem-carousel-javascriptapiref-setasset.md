---
description: Carousel Viewer的JavaScript API参考。
seo-description: Carousel Viewer的JavaScript API参考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: 770cbb87-af86-48dc-88a0-e74f6716f545
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---


# setAsset{#setasset}

Carousel Viewer的JavaScript API参考。

` setAsset( *`asset`*)`

设置新资产。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用它，则查看器在运行时交换资产。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}新资产ID。 </p> <p>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像参考：

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

