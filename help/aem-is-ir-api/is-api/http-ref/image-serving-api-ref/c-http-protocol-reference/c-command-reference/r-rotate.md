---
title: 旋转
description: 旋转图像。 将图像、文本或纯色图层旋转指定的角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# 旋转{#rotate}

旋转图像。 将图像、文本或纯色图层旋转指定的角度。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度，以度为单位（实数）。 </p></td> 
 </tr> 
</table>

正角度顺时针旋转。 图层锚点（`anchor=`或`catalog::Anchor`）用作旋转中心。 该图层矩形被放大并且根据需要围绕旋转的数据进行嵌合，以避免裁切。 使用`color=`填充图层的背景区域后应用旋转。 修饰符`bgColor=`可用于在旋转后向边界矩形添加背景颜色。

## 属性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

图层命令。 应用于当前图层，或应用于图层0（如果为`layer=comp`）。 被效果层忽略。

## 默认 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，表示无轮换。

## 示例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在图像目录中的图像的左上角附近放置“待售”标签。 标签图像的大小已适用于300x300视图，应该向左旋转30°。 要增强标签，请使用白色、半不透明的颜色填充文本框。

`http:// *`服务器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

将`size=`应用于图层0以设置视图大小，而不是使用`wid=`和`hei=`。 此方法允许在不更改`labelImage`的最终大小的情况下调整`myImageId`的大小。 此外，请指定`scl=1`，否则复合图像可能会缩放到`attribute::DefaultPix`（除非该图像设置为0,0）。 修饰符`color=`在旋转之前将半不透明的背景颜色添加到文本框。

两个图层的原点都设置为左上角，以实现所需的对齐。 图层1的原点在旋转后应用于`labelImage`。

有关旋转文本的示例，请参阅[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的[示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)。

## 另请参阅 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
