---
title: 目錄屬性檔案
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 任何文字編輯器都可以隨時維護這些文字。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有 `.ini` 檔案字尾。 任何文字編輯器都可以隨時維護這些文字。

目錄屬性檔案由一組文字記錄組成，以單一分隔 `<CR>` （ASCII代碼0xD），單 `<LF>` （ASCII代碼0xA）或 `<CR><LF>` 配對。 每個記錄都包含一個屬性名稱以及一或多個以逗號分隔的屬性值：

`*`名稱`*= *`值`*&#42;[, *`值`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性名稱；可能包含一或多個字母、數字、'-'和'_'；不區分大小寫。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>屬性值；不得包含 <span class="codeph"> &lt;cr&gt; </span>，或 <span class="codeph"> &lt;lf&gt; </span> 字元，除非在新行字元前有一個反斜線逸出。 </p> </td> 
 </tr> 
</table>

* Token之間的空白字元為選用。
* 具有未知屬性名稱的記錄會被 [!DNL Platform Server].
* 屬性名稱可包含ASCII字母、數字和「 — 」、「_」和「。」的任意組合。
* 如果相同的屬性名稱在相同的屬性檔案中出現多次，則會以最後一個出現的屬性名稱為準。
* 使用&#39;#&#39;作為第一個字元，將任何記錄標籤為剖析器忽略的註解。
