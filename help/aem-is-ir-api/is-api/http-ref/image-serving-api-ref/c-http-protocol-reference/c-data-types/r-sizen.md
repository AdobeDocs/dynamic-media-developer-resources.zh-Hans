---
description: 标准化大小。 用于指定图像大小或矩形大小，相对于图层0或其他图像的大小进行标准化。
seo-description: 标准化大小。 用于指定图像大小或矩形大小，相对于图层0或其他图像的大小进行标准化。
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sizeN{#sizen}

标准化大小。 用于指定图像大小或矩形大小，相对于图层0或其他图像的大小进行标准化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> nx <span class="varname"></span> , </span><span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> nx <span class="varname"></span> , </span><span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>相对于另一个图像（实数、实数、大于0）的标准化宽度和高度 </p></td> 
 </tr> 
</table>

*nx**和* ny必须大于0。 0,0可能指示应使用特定的默认大小。 1,1指定与参考图像相等的大小。
