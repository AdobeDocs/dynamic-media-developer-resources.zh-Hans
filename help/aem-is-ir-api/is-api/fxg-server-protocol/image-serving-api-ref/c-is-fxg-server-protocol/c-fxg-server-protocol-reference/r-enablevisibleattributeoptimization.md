---
description: 啟用FXG的最佳化。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

啟用FXG的最佳化。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Enablevisibleattributeoptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

移除在FXG中可見度設為false的元素，同時傳遞此FXG，進而減少FXG的處理時間。 但只會移除可見度顯示為false的元素，而不會影響FXG中的任何其他元素。 例如，如果文字位於 `Path` 和可見度 `Path` 設為false，則即使啟用此修飾元，也不會從FXG中移除它，因為需要在此路徑上繪製文字。

默认值为 1。
