---
description: 支持优化FXG。
seo-description: 支持优化FXG。
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

支持优化FXG。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

在传递此FXG时，删除其可见性在FXG中设置为false的元素，这反过来又减少了FXG的处理时间。 尽管它只删除那些可见性为false且不会影响FXG中任何其他元素的元素。 例如，如果`Path`上存在文本，并且`Path`的可见性设置为false，则即使启用了此修饰符，也不会从FXG中删除它，因为需要在此路径上绘制文本。

默认值为 1。
