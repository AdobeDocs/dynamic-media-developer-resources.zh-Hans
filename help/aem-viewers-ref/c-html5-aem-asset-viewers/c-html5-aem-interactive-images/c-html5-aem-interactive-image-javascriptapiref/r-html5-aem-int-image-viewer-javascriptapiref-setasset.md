---
description: Video Image Viewer的JavaScript API参考。
seo-description: Video Image Viewer的JavaScript API参考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---


# setAsset{#setasset}

Video Image Viewer的JavaScript API参考。

` setAsset( *`asset`*)`

设置新资产。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用它，则查看器会在运行时交换资产。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}个新资产ID。 </p> <p>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像参考：

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

