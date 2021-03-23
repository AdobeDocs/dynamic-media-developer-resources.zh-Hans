---
description: 创建一个固定大小的模板，包括静态背景图像、一个与左中心背景对齐且缩放为不超过背景宽度和高度的80%的可变图像，以及一个文本图层，其中垂直文本居中在画布的右边缘。
seo-description: 创建一个固定大小的模板，包括静态背景图像、一个与左中心背景对齐且缩放为不超过背景宽度和高度的80%的可变图像，以及一个文本图层，其中垂直文本居中在画布的右边缘。
seo-title: 示例A
solution: Experience Manager
title: 示例A
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---


# 示例A{#example-a}

创建一个固定大小的模板，包括静态背景图像、一个与左中心背景对齐且缩放为不超过背景宽度和高度的80%的可变图像，以及一个文本图层，其中垂直文本居中在画布的右边缘。

![](assets/examplea.png)

## 模板记录{#section-32f54710593e438fa0622224c89380af}

插入对象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;layer=2&amp;$text=layer+2+goes+此处文本=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

所有图层的`origin=`值在模板中显式指定，以严格控制图层的定位和对齐。 每个图层来源设置为与该图层的所需对齐匹配。 背景（层0）的`origin=`设置为中心；这是任意的，因为背景图像在运行时不会更改；可以使用图层0来源的任何值。

`pos=`值提供图层来源点之间的必要偏移，以实现所需的图层定位。

第1层图像的锚点位于左中心；结合`pos=`值，这实现背景和第1层图像之间的左中心对齐，而不管第1层图像的高宽比如何。

同样，文本图层的锚点位于自动调整大小文本框的右中心。 与pos=结合使用，可独立于字体大小和字符串长度实现旋转文本所需的右中心对齐。

实际显示文本将在运行时提供，因此使用变量将文本与rtf格式封套分开。 对于第1层图像，我们使用默认变量`$object`。 这允许在请求路径中指定此图像。

任何图像都可用于背景图像和第1层图像。 如果背景图像具有蒙版，则未蒙版区域将用默认背景颜色(`attribute::BkgColor`)填充，或在`fmt=png-alpha`或`fmt=tif-alpha`时为左透明。 如果背景图像具有非方形长宽比，则背景图像居中在回复图像中，并且额外空间填充`attribute::BkgColor`。 如果第1层图像具有Alpha数据或蒙版，则背景图像（或背景颜色）在透明区域中将保持可见。 如果图像没有蒙版，它将填充整个分配的矩形。

## 使用模板{#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下图显示了图层1图像的不同长宽比和不同文本字符串的复合结果。

![](assets/exampleausing.png)

