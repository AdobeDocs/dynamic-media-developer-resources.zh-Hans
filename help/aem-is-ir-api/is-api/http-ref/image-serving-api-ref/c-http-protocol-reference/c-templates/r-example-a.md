---
title: 示例A
description: 使用静态背景图像创建固定大小的模板，该静态背景图像是与背景在左中心对齐的可变图像，可缩放到不超过背景宽度和高度的80%。 最后，一个文本图层，垂直文本居中在画布的右边缘。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 示例A{#example-a}

使用静态背景图像创建固定大小的模板，该静态背景图像是与背景在左中心对齐的可变图像，可缩放到不超过背景宽度和高度的80%。 最后，一个文本图层，垂直文本居中在画布的右边缘。

![示例图像](assets/examplea.png)

## 模板记录 {#section-32f54710593e438fa0622224c89380af}

插入对象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog：：Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog：：Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text+goes+here&amp;text=rtf.....rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0 </span> </p> </td> 
 </tr> 
</table>

此 `origin=` 所有层的值在模板中显式指定，以严格控制层的定位和对齐。 每个图层原点都设置为与该图层的所需对齐相匹配。 此 `origin=` 对于背景（图层0），设置为中心；该值是任意的，因为背景图像在运行时不会更改；可以使用图层0原点的任何值。

此 `pos=` 值提供图层原点之间的必要偏移，以实现所需的图层定位。

图层1图像的锚点位于左中央，且 `pos=` 值。 此设置实现了背景与第1层图像之间的左中对齐，而不管第1层图像的纵横比如何。

同样，文本图层的锚点位于自动调整大小的文本框的右中，并且 `pos=` 值。 此设置实现了所需旋转文本的右中对齐，而与字体大小和字符串长度无关。

实际显示文本在运行时提供，因此使用变量将文本与rtf格式信封分离。 默认变量 `$object` 用于第1层图像。 通过此变量，您可以在请求路径中指定此图像。

任何图像都可用于背景图像和图层1图像。 如果背景图像具有蒙版，则未蒙版区域会使用默认的背景颜色( `attribute::BkgColor`)，或保留为透明，当 `fmt=png-alpha` 或 `fmt=tif-alpha`. 如果背景图像具有非正方形纵横比，则它将在回复图像中居中，并且额外的空间会填充 `attribute::BkgColor`. 如果图层1图像具有Alpha数据或蒙版，则背景图像（或背景颜色）在透明区域中保持可见。 如果图像没有蒙版，则会填充整个分配的矩形。

## 使用模板 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下图显示了图层1图像和不同文本字符串的不同宽高比的合成结果。

![示例复合结果图像](assets/exampleausing.png)
