---
description: 旋转图像。 将图像、文本或纯色图层按指定角度旋转。
seo-description: 旋转图像。 将图像、文本或纯色图层按指定角度旋转。
seo-title: 旋转
solution: Experience Manager
title: 旋转
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# rotate{#rotate}

旋转图像。 将图像、文本或纯色图层按指定角度旋转。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度（以度为单位）。 </p></td> 
 </tr> 
</table>

正角度顺时针旋转。 图层锚点( `anchor=` 或 `catalog::Anchor`)用作旋转中心。 该层矩形根据需要被放大并配合在旋转的数据周围以避免裁切。 在用填充图层的背景区域后应用旋转 `color=`。 `bgColor=` 可用于在旋转后向定界矩形添加背景色。

## 属性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

图层命令。 应用于当前层，或应用于层0（如果） `layer=comp`。 被效果图层忽略。

## 默认 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，不旋转。

## 示例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在图像目录中图像的左上角附近放置一个“销售中”标签。 标签图像的大小已经对于300x300视图正确，应向左旋转30度。 用白色的半不透明颜色填充文本框以增强标签。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我们应 `size=` 用到第0层来设置视图大小，而不是使用 `wid=` 和 `hei=`。 这允许 `myImageId` 在不更改最终大小的同时调整大小 `labelImage`。 我们还需要指 `scl=1`定，否则，合成图像可能会缩放到 `attribute::DefaultPix` （除非设置为0,0）。 `color=` 在旋转之前，将半不透明背景色添加到文本框。

两个图层的来源均设置为左上角，以实现所需的对齐。 请注意，图层1的来源点在旋转 `labelImage`后应用于该点。

有 [关旋转文本的](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 示例，请参 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 阅模板中的示例A。

## 另请参阅 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
