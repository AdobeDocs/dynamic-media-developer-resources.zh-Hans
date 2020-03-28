---
description: Video360查看器的JavaScript API参考。
seo-description: Video360查看器的JavaScript API参考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: db1321fb-6d52-4add-8877-0c13eb12e6af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Video360查看器的JavaScript API参考。

`setAsset(asset)`

设置新资产。 您可以在之前或之后随时调用此参数 `init()`。 如果在之后调用它， `init()`则查看器会在运行时交换资产。

另请参阅 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新资产ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```

