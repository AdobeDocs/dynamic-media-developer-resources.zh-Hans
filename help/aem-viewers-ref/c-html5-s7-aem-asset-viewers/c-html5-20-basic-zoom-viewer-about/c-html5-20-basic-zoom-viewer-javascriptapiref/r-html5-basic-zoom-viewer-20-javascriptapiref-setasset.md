---
title: setAsset
description: 基本缩放查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
TQID: 'https://experienceleague.adobe.com/mFCCdKYPrxPYCXtPDeU9ftxA3vlnVHrJXFOuHJiwtHg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 2%

---

# setAsset{#setasset}

基本缩放查看器的JavaScript API参考。

` setAsset( *`资源`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">资源</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}新资产ID，具有附加在“？”后面的可选IS修饰符 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资源。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用，则查看器会在运行时交换资源。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像引用：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

向集中的所有图像添加了锐化修饰符：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```
