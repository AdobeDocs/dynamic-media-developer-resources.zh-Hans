---
description: 标准化大小。 用于指定图像大小或矩形大小，与图层0或其他图像的大小进行标准化。
seo-description: 标准化大小。 用于指定图像大小或矩形大小，与图层0或其他图像的大小进行标准化。
seo-title: sizeN
solution: Experience Manager
title: sizeN
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# sizeN{#sizen}

标准化大小。 用于指定图像大小或矩形大小，与图层0或其他图像的大小进行标准化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>相对于另一个图像（实数、实数、大于0）的标准化宽度和高度 </p></td> 
 </tr> 
</table>

*nx*&#x200B;和&#x200B;*ny*&#x200B;都必须大于0。 0,0可能指示应使用特定默认大小。 1,1指定与参考图像相等的大小。
