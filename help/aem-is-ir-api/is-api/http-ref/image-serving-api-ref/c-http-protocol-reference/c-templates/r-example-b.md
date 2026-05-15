---
description: 与示例A的要求类似，但使用纯色背景并允许复合物高度发生变化，以适应具有不同长宽比的图像。
solution: Experience Manager
title: 示例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
TQID: 'https://experienceleague.adobe.com/nwRD9lmoHIjjFR32pdr0g6jRpsIIZicZXmVBXC74ot4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# 示例B{#example-b}

与示例A的要求类似，但使用纯色背景并允许复合物高度发生变化，以适应具有不同长宽比的图像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">目录：：Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">目录：：Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

图像放置在图层0中，高度值`size=`设置为0。 此设置使实际高度由图像缩放到800像素宽后的高度来确定。

变量`extend=`在顶部和底部添加100像素，在右侧添加200像素。

图层0和图层1的原点都位于合成区域的右中央，以获得所需的文本位置。

下图显示了图像与不同文本字符串的不同宽高比的合成结果。

![示例B图像](assets/exampleb.png)
