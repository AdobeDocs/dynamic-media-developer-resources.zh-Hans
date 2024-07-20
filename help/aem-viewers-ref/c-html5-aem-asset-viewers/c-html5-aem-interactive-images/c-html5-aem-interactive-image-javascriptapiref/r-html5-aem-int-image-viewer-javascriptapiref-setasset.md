---
title: setAsset
description: 视频图像查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# setAsset{#setasset}

视频图像查看器的JavaScript API参考。

` setAsset( *`资源`*)`

设置新资源。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用，则查看器会在运行时交换资源。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">资源</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}新资产ID。 </p> <p>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像引用：

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
