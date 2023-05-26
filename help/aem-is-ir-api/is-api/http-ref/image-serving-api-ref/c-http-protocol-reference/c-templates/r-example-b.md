---
description: 与示例A的要求类似，但使用纯色背景并允许复合物的高度发生变化，以适应具有不同长宽比的图像。
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

与示例A的要求类似，但使用纯色背景并允许复合物的高度发生变化，以适应具有不同长宽比的图像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

图像放置在图层0中，高度值为 `size=` 设置为0。 此设置使实际高度由图像缩放到800像素宽后的高度确定。

变量 `extend=` 将顶部和底部添加100像素，将右侧添加200像素。

图层0和图层1的原点都放在合成区域的右中角，以获得所需的文本位置。

下图显示了图像与不同文本字符串的不同宽高比的合成结果。

![示例B图像](assets/exampleb.png)
