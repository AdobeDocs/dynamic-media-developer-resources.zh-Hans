---
description: 混合媒体查看器的JavaScript API参考。
seo-description: 混合媒体查看器的JavaScript API参考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

混合媒体查看器的JavaScript API参考。

` setAsset( *`asset`*[,data]))`

设置新资产和可选的其他资产数据。 您可以在之前或之后随时调用此参数 `init()`。 如果在之后调用它， `init()`则查看器会在运行时交换资产。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`asset`*` - { `String`}新资产ID或显式混合媒体集，后面附加可选的图像服务修饰符 `?`。

此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

` *`data`*` - { `JSON`}新题注文件的位置。

如果未指定，则描述按钮在用户界面中不可见。 使用此参数指定的字幕适用于混合媒体集中最先出现的视频；后续视频播放时不带字幕。 此查看器支持以下组件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件ID </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK组件类名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 后验图像 </span> </p> </td> 
   <td colname="col2"> <p>要在视频开始播放之前在第一帧上显示的图像。 </p> <p>请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> 阅VideoPlayer.posterimage </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字幕 </span> </p> </td> 
   <td colname="col2"> <p> 新题注文件的位置。 </p> <p>如果未指定，则描述按钮在用户界面中不可见。 使用此参数指定的字幕适用于媒体集中最先出现的视频。 后续视频播放时不带字幕。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单媒体集参考：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

显式媒体集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

锐化修饰符已添加到集合中的所有图像：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

