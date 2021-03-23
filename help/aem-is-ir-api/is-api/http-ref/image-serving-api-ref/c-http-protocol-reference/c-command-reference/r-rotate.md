---
description: 旋转图像。 将图像、文本或纯色图层旋转指定角度。
seo-description: 旋转图像。 将图像、文本或纯色图层旋转指定角度。
seo-title: 旋转
solution: Experience Manager
title: 旋转
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 3%

---


# rotate{#rotate}

旋转图像。 将图像、文本或纯色图层旋转指定角度。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度（以度为单位）。 </p></td> 
 </tr> 
</table>

正角顺时针旋转。 图层锚点（`anchor=`或`catalog::Anchor`）用作旋转中心。 根据需要放大并拟合图层矩形以避免裁切。 在用`color=`填充图层的背景区域后应用旋转。 `bgColor=` 可用于在旋转后向定界矩形添加背景颜色。

## 属性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

图层命令。 应用于当前图层，或应用于`layer=comp`时的图层0。 被效果图层忽略。

## 默认 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，不旋转。

## 示例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在图像目录中图像的左上角附近放置一个“销售中”标签。 标签图像的大小已正确适用于300x300视图，应向左旋转30度。 用白色半不透明颜色填充文本框以增强标签。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我们将`size=`应用到层0以设置视图大小，而不是使用`wid=`和`hei=`。 这允许在不更改`labelImage`的最终大小时调整`myImageId`的大小。 我们还需要指定`scl=1`，否则可能会将复合图像缩放为`attribute::DefaultPix`（除非该图像设置为0,0）。 `color=` 在旋转之前，将半不透明背景颜色添加到文本框。

两个图层的来源均设置为左上角，以实现所需的对齐。 请注意，图层1的来源点在旋转后应用于`labelImage`。

有关旋转文本的示例，请参见[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另请参阅 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
