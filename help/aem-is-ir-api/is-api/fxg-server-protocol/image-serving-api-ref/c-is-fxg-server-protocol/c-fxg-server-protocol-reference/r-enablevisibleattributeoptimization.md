---
description: 支持FXG的优化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

支持FXG的优化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

在传递此FXG时，删除其可见性在FXG中设置为false的元素，这进而会缩短FXG的处理时间。 但是，它只会删除可见性为false且不会影响FXG中任何其他元素的那些元素。 例如，如果`Path`上存在文本，并且`Path`的可见性设置为false，则即使启用了此修饰符，也不会从FXG中删除该文本，因为需要在此路径上绘制文本。

默认值为 1。
