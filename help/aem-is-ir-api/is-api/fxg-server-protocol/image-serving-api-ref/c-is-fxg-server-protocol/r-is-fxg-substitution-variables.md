---
description: 替代變數可用來將值從請求URL傳輸到儲存在伺服器上的FXG範本。
solution: Experience Manager
title: 替代變數
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 替代變數{#substitution-variables}

替代變數可用來將值從請求URL傳輸到儲存在伺服器上的FXG範本。

` $ *`var`*= *`值`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>變數名稱。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>變數要設定的值（字串）。 </p> </td> 
 </tr> 
</table>

* 變數定義和參照可能會出現在請求URL的查詢部分中。
* 變數的定義如上所述，與其他IS命令類似；前導的「$」會將該命令識別為變數定義。
* 變數名稱 `*`var`*` 區分大小寫，並可由字母、數字、&#39;-&#39;和&#39;_&#39;的任意組合組成。
* 重要值必須為單次URL編碼，才能安全HTTP傳輸。
