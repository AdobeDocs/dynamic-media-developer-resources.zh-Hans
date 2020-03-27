---
description: 支持FXG的优化。
seo-description: 支持FXG的优化。
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

支持FXG的优化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

删除在FXG中其可见性设置为false的元素，同时传递此FXG，这进而减少了FXG的处理时间。 尽管它只删除那些可见性为false且不会影响FXG中任何其他元素的元素。 例如，如果存在文本， `Path` 且可见性设置为 `Path` false，则即使启用了此修饰符，也不会从FXG中删除它，因为需要在此路径上绘制文本。

默认值为 1。
