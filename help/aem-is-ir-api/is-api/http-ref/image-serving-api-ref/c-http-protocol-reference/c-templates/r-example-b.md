---
description: 与示例A类似的要求，但使用纯色背景并允许复合图像的高度发生变化，以适应宽高比不同的图像。
solution: Experience Manager
title: 示例B
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 示例B{#example-b}

与示例A类似的要求，但使用纯色背景并允许复合图像的高度发生变化，以适应宽高比不同的图像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 目录：:Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 目录：：修饰符</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp;layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf...$text$.....rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

图像放置在图层0中，高度值`size=`设置为0，这会导致实际高度由图像在缩放到800像素宽后的高度决定。

`extend=` 在顶部和底部添加100像素，在右侧添加200像素。

层0和层1的原点都位于合成区域的中右侧，以达到所需的文本位置。

下图显示了图像和不同文本字符串的不同长宽比的复合结果。

![](assets/exampleb.png)
