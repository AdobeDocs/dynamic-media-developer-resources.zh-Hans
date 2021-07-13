---
description: Photoshop样式的层阴影和发光效果是使用特殊子层（效果层）实现的，子层可附加到任何层（父层），包括layer=0和layer=comp。
solution: Experience Manager
title: 图层效果
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 2%

---

# 图层效果{#layer-effects}

Photoshop样式的层阴影和发光效果是使用特殊子层（效果层）实现的，子层可附加到任何层（父层），包括layer=0和layer=comp。

尽管效果层支持许多标准图像和层属性及命令，但它们不是通用层，也不支持独立的图像或文本数据。

任何数量的层效果都可以附加到单个父层。

## 内外效果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*内部* 效果呈现在父层的顶部，并且仅在父层的不透明区域中可见。*外部* 效果呈现在父层之后（因此它们在父层的不透明区域内永远不可见），并且可以位于复合画布内的任意位置。通过使用`effect=`命令指定正或负效应层数来选择内或外效应。 `effect=`命令还控制连接到同一父层的多个效果层之间的z顺序。

## 与父层的关系 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

自动调整效果层的大小并将其定位为与父层一致（即，效果层继承父层的`size=`和`origin=`值）。 `pos=` 可用于将效果图层从父图层移开，这是投影和内部阴影效果通常所需的操作。而对于标准层`pos=`指定此层的源与层0之间的偏移，对于效果层`pos=`指定效果层的源与父层之间的偏移。

## 支持的命令和属性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果层接受以下命令和属性：

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

## 默认效果宏 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

为了方便使用图层效果，IS提供了两个带有默认图像目录（`$shadow$`和`$glow$`）的宏，这两个宏为与Photoshop图层效果类似的效果图层属性提供默认值。 下表列出了实施默认层效果时应使用的效果命令和宏。 自然，宏中指定的任何属性都可以在URL中修改，或者也可以创建替代宏以实施自定义层效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 预期效果</b> </th> 
   <th class="entry"> <b> 命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 投影 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
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

边框将跟随图像的Alpha通道或蒙版的轮廓。 设置`effect=1`会将边框放置在内边缘上。

使用默认效果设置（颜色除外）将蓝色投影添加到图像：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 向图像右下边缘添加一小段距，以防止将投影剪切到图像范围。

## 另请参阅 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)，命 [令宏%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
