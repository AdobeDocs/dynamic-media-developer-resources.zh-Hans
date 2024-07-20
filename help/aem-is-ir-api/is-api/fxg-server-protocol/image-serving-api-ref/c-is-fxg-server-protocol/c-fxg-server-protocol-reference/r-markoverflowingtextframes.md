---
description: 显示带加号的溢流文本框架。 当文本超出文本框架中为其分配的空间（如果是串连文本，则为最后一个文本框架）时，将显示文本溢出指示符。 指示器是一个红色的框，上面有一个加号。
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

显示带加号的溢流文本框架。 当文本超出文本框架中为其分配的空间（如果是串连文本，则为最后一个文本框架）时，将显示文本溢出指示符。 指示器是一个红色的框，上面有一个加号。

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

通过URL调用设置修饰符`markOverflowingTextFrames=1`将用加号标记文本溢流的所有文本框架。 此外，在Dynamic Media Classic预览器中，文本溢排指示符默认设置为“`TRUE`”。

默认值为 0。
