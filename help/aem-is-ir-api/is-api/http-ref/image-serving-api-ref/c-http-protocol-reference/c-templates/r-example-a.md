---
title: 示例A
description: 创建具有静态背景图像的固定大小模板，该背景图像是与左中心的背景对齐的变量图像，可缩放为不超过背景宽度和高度的80%。 最后，一个文本层，垂直文本居中在画布的右边。
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

创建具有静态背景图像的固定大小模板，该背景图像是与左中心的背景对齐的变量图像，可缩放为不超过背景宽度和高度的80%。 最后，一个文本层，垂直文本居中在画布的右边。

![图像示例](assets/examplea.png)

## 模板记录 {#section-32f54710593e438fa0622224c89380af}

插入对象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目录：:Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目录：：修饰符  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=+ges+here&amp;text=......$text......&amp;rotate=-90&amp;origin=0.5,rtf=0.n=0.0  </span> </p> </td> 
 </tr> 
</table>

所有层的`origin=`值在模板中显式指定，以严格控制层的定位和对齐。 每个层原点设置为匹配该层的所需对齐方式。 背景（层0）的`origin=`设置为中心；此值是任意的，因为背景图像在运行时不会更改；可以使用层0原点的任何值。

`pos=`值在层原点之间提供必要的偏移，以实现所需的层定位。

第1层图像的锚点位于左中心，其值为`pos=`。 该设置实现背景和第1层图像之间的左中心对齐，而不管第1层图像的宽高比。

同样，文本层的锚点位于自动调整大小文本框的右中心，其值为`pos=` 。 此设置可实现旋转文本所需的右居中对齐方式，与字体大小和字符串长度无关。

在运行时提供实际的显示文本，因此使用变量将文本与rtf格式信封分隔开。 默认变量`$object`用于第1层图像。 此变量允许您在请求路径中指定此图像。

任何图像都可用于背景图像和第1层图像。 如果背景图像具有蒙版，则未蒙版区域将使用默认背景颜色(`attribute::BkgColor`)填充，或在`fmt=png-alpha`或`fmt=tif-alpha`时使其保持透明。 如果背景图像具有非正方形宽高比，则在回复图像中居中，并且额外的空间填充`attribute::BkgColor`。 如果第1层图像具有Alpha数据或蒙版，则背景图像（或背景颜色）在透明区域中保持可见。 如果图像没有蒙版，则它将填充整个分配的矩形。

## 使用模板 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下图显示了第1层图像不同纵横比和不同文本字符串的复合结果。

![示例复合结果图像](assets/exampleausing.png)
