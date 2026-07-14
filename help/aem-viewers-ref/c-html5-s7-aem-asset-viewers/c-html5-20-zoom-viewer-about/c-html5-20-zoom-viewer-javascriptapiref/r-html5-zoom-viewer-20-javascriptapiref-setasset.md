---
title: setAsset
description: 视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
TQID: 'https://experienceleague.adobe.com/WSUZln6WtAUoNCL-BsnmGg9PKJw-8T5ozloMvzTyzuo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 1%

---

# setAsset{#setasset}

视频查看器的JavaScript API参考。

` setAsset( *`资源`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">资源</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}包含新资产ID、显式图像集或显式图像集（具有特定于帧的图像服务修饰符），并在“？”后附加可选的全局图像服务修饰符。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资源。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用，则查看器会在运行时交换资源。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像引用，如下所示：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

对目录中定义的图像集的单个引用，如下所示：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

按如下方式设置显式图像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用帧特定的图像服务修饰符设置的显式图像，如下所示：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

向集中的所有图像添加了锐化修饰符，如下所示：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

