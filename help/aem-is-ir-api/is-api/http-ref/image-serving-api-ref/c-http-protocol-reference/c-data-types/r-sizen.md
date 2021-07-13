---
description: 标准化大小。 用于指定图像大小或矩形大小，相对于图层0的大小或某些其他图像的大小进行标准化。
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# sizeN{#sizen}

标准化大小。 用于指定图像大小或矩形大小，相对于图层0的大小或某些其他图像的大小进行标准化。

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>相对于另一图像（实、实、大于0）的标准化宽度和高度 </p></td> 
 </tr> 
</table>

*nx*&#x200B;和&#x200B;*ny*&#x200B;必须大于0。 0,0可能表示应使用特定的默认大小。 1,1指定大小等于参考图像。
