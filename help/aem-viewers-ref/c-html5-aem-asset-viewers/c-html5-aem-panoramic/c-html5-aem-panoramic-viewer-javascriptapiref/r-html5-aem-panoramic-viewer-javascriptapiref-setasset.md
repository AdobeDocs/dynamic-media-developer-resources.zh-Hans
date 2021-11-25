---
title: setAsset
description: 全景查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# setAsset{#setasset}

全景查看器的JavaScript API引用。

`setAsset(asset)`

设置新资产。 您可以在之前或之后随时调用此参数 `init()`. 如果在 `init()`，则查看器会在运行时交换资产。

另请参阅 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 字符串</span>}新资产id。 此查看器不支持使用图像渲染(IR)或用户生成内容(UGC)的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
