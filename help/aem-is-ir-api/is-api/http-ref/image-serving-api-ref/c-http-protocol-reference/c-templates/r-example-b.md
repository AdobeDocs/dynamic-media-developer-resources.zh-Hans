---
description: 与示例A类似的要求，但使用纯色背景，并允许合成的高度发生变化，以适应长宽比不同的图像。
seo-description: 与示例A类似的要求，但使用纯色背景，并允许合成的高度发生变化，以适应长宽比不同的图像。
seo-title: 示例B
solution: Experience Manager
title: 示例B
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 示例B{#example-b}

与示例A类似的要求，但使用纯色背景，并允许合成的高度发生变化，以适应长宽比不同的图像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp;layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

图像放置在图层0中，并且高度值`size=`设置为0，这样，在将图像缩放为800像素宽后，实际高度由图像的高度确定。

`extend=` 在顶部和底部添加100像素，在右侧添加200像素。

图层0和图层1的来源均位于合成区域的中右侧，以达到所需的文本位置。

下图显示了图像和不同文本字符串的不同长宽比的合成结果。

![](assets/exampleb.png)

