---
title: 图层效果
description: Photoshop样式的图层阴影和辉光效果是使用特殊子图层（效果图层）实现的，这些子图层可以附加到任何图层（父图层），包括layer=0和layer=comp。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# 图层效果{#layer-effects}

Photoshop样式的图层阴影和辉光效果是使用特殊子图层（效果图层）实现的，这些子图层可以附加到任何图层（父图层），包括layer=0和layer=comp。

虽然效果图层支持许多标准图像和图层属性及命令，但它们不是用于一般用途的图层，并且不支持独立的图像或文本数据。

可以将任意数量的图层效果附加到单个父图层。

## 内部和外部效果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*内部效果*&#x200B;呈现在父图层的顶部，并且仅在父图层的不透明区域中可见。 *外部效果*&#x200B;在父图层后面渲染（因此它们永远不会在父图层的不透明区域中可见），并且可以在合成画布中的任意位置放置。 通过使用`effect=`命令指定正或负效果层数来选择内部或外部效果。 `effect=`命令还控制连接到同一父层的多个效果层之间的z排序。

## 与父层的关系 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

效果图层会自动调整大小并定位为与父图层一致（即，效果图层会继承父图层的`size=`和`origin=`值）。 `pos=`可用于将效果图层从父图层移开，这通常是投影和内阴影效果所必需的。 对于标准图层`pos=`指定此图层的源与图层0之间的偏移，对于效果图层`pos=`指定效果图层的源与父图层之间的偏移。

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

将忽略效果图层中包含的所有其他图像和图层命令。

## 默认效果宏 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

为便于使用图层效果，IS提供了两个带有默认图像目录`$shadow$`和`$glow$`的宏，这两个宏为效果图层属性提供了与Photoshop图层效果类似的默认值。 下表列出了实施默认图层效果时应使用的效果命令和宏。 当然，可以在URL中修改宏中指定的任何属性，也可以创建其他宏以实现自定义图层效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>所需效果</b> </th> 
   <th class="entry"> <b>命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 投影 </p> </td> 
   <td> <p> <span class="codeph">效果=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内阴影 </p> </td> 
   <td> <p> <span class="codeph">效果=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 外发光 </p> </td> 
   <td> <p> <span class="codeph">效果=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内发光 </p> </td> 
   <td> <p> <span class="codeph">效果=1&amp;$发光$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-4c449fdf707b43858917fb271fa1fe96}

向图层添加一个具有50%不透明度的3像素宽红色边框：

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

边框遵循图像的Alpha通道或蒙版的轮廓。 设置`effect=1`会将边框放在内边缘上。

使用默认效果设置（颜色除外）为图像添加蓝色投影：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=`在图像的右下边缘添加了一小段边距，这样可防止投影被剪切到图像边界上。

## 另请参阅 {#section-1acccccf534549aea23d4c008c17e7c0}

[效果=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)，[命令宏%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
