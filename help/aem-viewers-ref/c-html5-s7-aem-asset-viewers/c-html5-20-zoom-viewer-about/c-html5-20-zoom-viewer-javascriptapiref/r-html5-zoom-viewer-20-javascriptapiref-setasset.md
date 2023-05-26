---
title: setAsset
description: 视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# setAsset{#setasset}

视频查看器的JavaScript API参考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 字符串 </span>}新资源id、显式图像集或显式图像集，带有特定于帧的图像服务修饰符，并在“？”后附加可选的全局图像服务修饰符。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资源。 您可以随时在之前或之后调用此参数 `init()`. 如果在之后调用 `init()`时，查看器会在运行时交换资源。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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

显式图像集，如下所示：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用特定于帧的图像服务修饰符显式设置图像，如下所示：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

锐化修饰符已添加到集中的所有图像，如下所示：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
