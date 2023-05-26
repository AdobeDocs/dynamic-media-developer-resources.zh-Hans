---
title: setAsset
description: 适用于混合媒体查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

适用于混合媒体查看器的JavaScript API引用。

` setAsset( *`asset`*[,data]))`

设置新资源和可选的其他资源数据。 您可以随时在之前或之后调用此参数 `init()`. 如果在之后调用 `init()`时，查看器会在运行时交换资源。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`资产`*` - { `String`}个新资产ID或显式混合媒体集，并在后面附加可选的图像服务修饰符 `?`.

此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

`*`数据`*` - { `JSON`新字幕文件的}位置。

如果未指定，则说明按钮在用户界面中不可见。 使用此参数指定的字幕适用于混合媒体集中排名靠前的视频；后续播放的视频不含字幕。 此查看器支持以下组件ID：

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件Id </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK组件类名称 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 后影像 </span> </p> </td> 
   <td colname="col2"> <p>在视频开始播放前的第一帧显示的图像。 </p> <p>参见 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 题注 </span> </p> </td> 
   <td colname="col2"> <p> 新字幕文件的位置。 </p> <p>如果未指定，则说明按钮在用户界面中不可见。 使用此参数指定的字幕适用于媒体集中排名第一的视频。 随后播放的视频不含字幕。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个媒体集引用：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

显式媒体集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

锐化修饰符已添加到集中的所有图像：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
