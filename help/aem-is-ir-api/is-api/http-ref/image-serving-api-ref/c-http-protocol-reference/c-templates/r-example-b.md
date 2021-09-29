---
description: 与示例A类似的要求，但使用纯色背景并允许复合图像的高度发生变化，以适应宽高比不同的图像。
solution: Experience Manager
title: 示例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
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
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp;layer=0&amp;size=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

图像放置在图层0中，并且`size=`的高度值设置为0。 此设置会在将图像宽度缩放为800像素后，将其实际高度由图像的高度确定。

变量`extend=`在顶部和底部添加100像素，在右侧添加200像素。

层0和层1的原点都位于合成区域的中右侧，以达到所需的文本位置。

下图显示了图像不同长宽比和不同文本字符串的复合结果。

![示例B图像](assets/exampleb.png)
