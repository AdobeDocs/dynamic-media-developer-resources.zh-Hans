---
description: 旋转图像。 按指定角度旋转图像、文本或纯色图层。
seo-description: 旋转图像。 按指定角度旋转图像、文本或纯色图层。
seo-title: 旋转
solution: Experience Manager
title: 旋转
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 4%

---


# rotate{#rotate}

旋转图像。 按指定角度旋转图像、文本或纯色图层。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度（以度为单位）。 </p></td> 
 </tr> 
</table>

正角度顺时针旋转。 层锚点（`anchor=`或`catalog::Anchor`）用作旋转中心。 根据需要，放大层矩形并围绕旋转的数据进行装配，以避免裁切。 在用`color=`填充图层的背景区域后应用旋转。 `bgColor=` 可用于在旋转后向定界矩形添加背景颜色。

## 属性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

图层命令。 应用于当前层，或应用于`layer=comp`时的层0。 被效果图层忽略。

## 默认 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, for no rotation.

## 示例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在图像目录中图像的左上角附近放置一个“售后”标签。 标签图像的大小已正确，适合300x300视图，应向左旋转30度。 用白色的半不透明颜色填充文本框以增强标签。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我们将`size=`应用到层0以设置视图大小，而不是使用`wid=`和`hei=`。 这允许在不更改最终大小`labelImage`时调整`myImageId`的大小。 我们还需要指定`scl=1`，否则，复合图像可能会缩放到`attribute::DefaultPix`（除非设置为0,0）。 `color=` 在旋转之前，将半不透明背景颜色添加到文本框。

两个图层的来源均设置在左上角，以实现所需的对齐。 请注意，层1的来源点在旋转后应用于`labelImage`。

有关旋转文本的示例，请参见[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另请参阅 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
