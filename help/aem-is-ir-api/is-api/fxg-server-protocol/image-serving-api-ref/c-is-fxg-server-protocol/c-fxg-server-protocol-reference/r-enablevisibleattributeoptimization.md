---
description: 启用FXG优化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

启用FXG优化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

删除在FXG中可见性设置为false的元素，同时传递此FXG，从而减少FXG的处理时间。 但它只删除可见性为false的元素，不会影响FXG中的任何其他元素。 例如，如果`Path`上有文本并且`Path`的可见性设置为false，那么即使启用此修饰符，它也不会从FXG中删除，因为需要在此路径上绘制文本。

默认值为 1。
