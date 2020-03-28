---
description: 使用静态背景图像创建一个固定大小的模板，一个在左中心与背景对齐并缩放为不超过背景宽度和高度的80%的可变图像，以及一个在画布右边缘居中的垂直文本的文本图层。
seo-description: 使用静态背景图像创建一个固定大小的模板，一个在左中心与背景对齐并缩放为不超过背景宽度和高度的80%的可变图像，以及一个在画布右边缘居中的垂直文本的文本图层。
seo-title: 示例A
solution: Experience Manager
title: 示例A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 示例A{#example-a}

使用静态背景图像创建一个固定大小的模板，一个在左中心与背景对齐并缩放为不超过背景宽度和高度的80%的可变图像，以及一个在画布右边缘居中的垂直文本的文本图层。

![](assets/examplea.png)

## 模板记录 {#section-32f54710593e438fa0622224c89380af}

插入对象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog:::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog:::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text+前往此处+text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

在模 `origin=` 板中显式指定所有图层的值，以严格控制图层的定位和对齐。 每个图层来源设置为与该图层的所需对齐方式相匹配。 背 `origin=` 景（0层）设置在中心；这是任意的，因为背景图像在运行时不会更改；可以使用图层0来源的任何值。

这些 `pos=` 值提供层来源点之间的必要偏移，以实现所需的层定位。

第1层图像的锚点位于左中心；结合值，这 `pos=` 实现了背景和第1层图像之间的左中心对齐，而不管第1层图像的长宽比如何。

同样，文本图层的锚点位于自动调整大小文本框的右中心。 与pos=结合使用，可独立于字体大小和字符串长度实现旋转文本所需的右中心对齐。

实际显示文本将在运行时提供，因此使用变量将文本与rtf格式封套分开。 我们对第1层图 `$object` 像使用默认变量。 这允许在请求路径中指定此图像。

任何图像都可用于背景图像和第1层图像。 如果背景图像有遮罩，则未遮罩的区域将填充默认背景色( `attribute::BkgColor`)，或在或时使其保持透 `fmt=png-alpha` 明 `fmt=tif-alpha`。 如果背景图像具有非方形长宽比，则背景图像居中在回复图像中，并填充额外的空间 `attribute::BkgColor`。 如果第1层图像具有alpha数据或蒙版，则背景图像（或背景颜色）在透明区域中将保持可见。 如果图像没有蒙版，它将填充所分配的整个矩形。

## 使用模板 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下图显示了图层1图像的不同长宽比和不同文本字符串的复合结果。

![](assets/exampleausing.png)

