---
description: Photoshop样式的图层阴影和发光效果是使用特殊的子图层（效果图层）实现的，这些子图层可以附加到任何图层（父图层），包括layer=0和layer=comp。
seo-description: Photoshop样式的图层阴影和发光效果是使用特殊的子图层（效果图层）实现的，这些子图层可以附加到任何图层（父图层），包括layer=0和layer=comp。
seo-title: 图层效果
solution: Experience Manager
title: 图层效果
uuid: 076e98de-cbbb-457b-984a-367a935b4356
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---


# 图层效果{#layer-effects}

Photoshop样式的图层阴影和发光效果是使用特殊的子图层（效果图层）实现的，这些子图层可以附加到任何图层（父图层），包括layer=0和layer=comp。

虽然效果图层支持许多标准图像和图层属性及命令，但它们不是通用图层，也不支持独立的图像或文本数据。

可以将任意数量的图层效果附加到单个父图层。

## 内外效果{#section-2dade7ee98e041d1b4d1725e6f98a515}

*内部* 效果渲染在父图层的顶部，并且仅在父图层的不透明区域中可见。*外部* 效果渲染在父图层之后（因此它们在父图层的不透明区域中永远不可见），并且可以放置在合成画布中的任意位置。通过使用`effect=`命令指定正或负效果图层编号来选择内或外效果。 `effect=`命令还控制连接到同一父图层的多个效果图层之间的z顺序。

## 与父层{#section-eb8bfc4f754a42fc973b562821d6f2d3}的关系

效果图层会自动调整大小并定位为与父图层一致（即，效果图层继承父图层的`size=`和`origin=`值）。 `pos=` 可用于将效果图层从父图层移开，这是投影和内部阴影效果通常需要的。对于标准图层`pos=`，指定此图层与图层0的来源之间的偏移，而对于效果图层`pos=`，指定效果图层与父图层的来源之间的偏移。

## 支持的命令和属性{#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果图层接受以下命令和属性：

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

效果图层中包含的所有其他图像和图层命令都将被忽略。

## 默认效果宏{#section-a01e8dcc87c94495b54a6dfb21d2a718}

为便于图层效果的使用，IS为默认图像目录`$shadow$`和`$glow$`提供了两个宏，它们为效果图层属性提供了与Photoshop图层效果类似的默认值。 应使用影响命令和宏的下表列表来实现默认图层效果。 自然，宏中指定的任何属性都可以在URL中修改，或者创建替代宏以实现自定义图层效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 所需效果</b> </th> 
   <th class="entry"> <b> 命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 投影 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadw$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内阴影 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 外发光 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内发光 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-4c449fdf707b43858917fb271fa1fe96}

向图层添加一个3个像素宽的红色边框，其不透明度为50%:

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

边框将沿图像的Alpha渠道或蒙版的等高线移动。 设置`effect=1`会将边框放置在内边。

使用默认效果设置（颜色除外）向图像添加蓝色投影：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 为图像的右下边缘添加一点边距，可防止将投影裁切到图像边界。

## 另请参阅 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)，命 [令宏%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
