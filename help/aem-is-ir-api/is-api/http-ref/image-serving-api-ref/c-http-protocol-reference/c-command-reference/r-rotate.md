---
title: 旋转
description: 旋转图像。 将图像、文本或纯色图层旋转指定的角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# 旋转{#rotate}

旋转图像。 将图像、文本或纯色图层旋转指定的角度。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度，以度为单位（实数）。 </p></td> 
 </tr> 
</table>

正角度顺时针旋转。 图层锚点( `anchor=` 或 `catalog::Anchor`)用作旋转中心。 该图层矩形被放大并且根据需要围绕旋转的数据进行嵌合，以避免裁切。 在填充图层的背景区域后应用旋转 `color=`. `bgColor=` 可用于在旋转后为边框矩形添加背景颜色。

## 属性 {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

图层命令。 应用到当前图层，或应用到图层0，如果 `layer=comp`. 被效果层忽略。

## 默认 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`，表示无轮换。

## 示例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

在图像目录中的图像的左上角附近放置“待售”标签。 标签图像已针对300x300视图正确调整大小，应该向左旋转30度。 使用白色、半不透明的颜色填充文本框以增强标签。

`http:// *`伺服器`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

我们申请 `size=` 到图层0以设置视图大小，而不是使用 `wid=` 和 `hei=`. 这允许 `myImageId` 以调整大小，同时不更改 `labelImage`. 我们还需要指定 `scl=1`，否则，复合图像可能会缩放到 `attribute::DefaultPix` （除非设置为0,0）。 `color=` 在旋转之前将半不透明的背景颜色添加到文本框。

两个层的原点都设置为左上角，以实现所需的对齐。 请注意，图层1的原点适用于 `labelImage`在它旋转之后。

请参阅 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 有关旋转文本的示例。

## 另请参阅 {#section-c371ee0845994b7382c02e782d1bc595}

[锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
