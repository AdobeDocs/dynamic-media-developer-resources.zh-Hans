---
description: 显示带加号的溢流文本框架。 当文本超出在文本框架内为其分配的空间（或者，如果是串接文本，则为在最后一个文本框架中分配的空间）时，会显示文本溢出指示符。该指示符是一个内含加号的红色方框。
solution: Experience Manager
title: markOverforingTextFrames
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 60%

---

# markOverforingTextFrames{#markoverflowingtextframes}

显示带加号的溢流文本框架。 当文本超出在文本框架内为其分配的空间（或者，如果是串接文本，则为在最后一个文本框架中分配的空间）时，会显示文本溢出指示符。该指示符是一个内含加号的红色方框。

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverforingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

通过URL调用设置修饰符`markOverflowingTextFrames=1`会用加号标记所有文本溢流的文本框架。 此外，在Dynamic Media Classic预览器中，默认情况下，文本溢流指示器设置为“ `TRUE`”。

默认值为 0。
