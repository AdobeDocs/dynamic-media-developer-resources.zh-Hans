---
description: 目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 任何文字編輯器都可以隨時維護這些文字。
solution: Experience Manager
title: 目錄屬性檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# 目錄屬性檔案{#catalog-attribute-files}

目錄屬性檔案可以有任何名稱，但必須有.ini檔案字尾。 任何文字編輯器都可以隨時維護這些文字。

目錄屬性檔案由一組文字記錄組成，以單一分隔 `<CR>` (ASCII程式碼 `0xD`)，單一 `<LF>` (ASCII程式碼 `0xA`)或 `<CR><LF>` 配對。 每個記錄都包含一個屬性名稱以及一或多個以逗號分隔的屬性值：

`*`名稱`*= *`值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 值</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[，<span class="varname"> 值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名称</span> </p> </td> 
  <td class="stentry"> <p>屬性名稱。 可能包含一或多個字母、數字、 — 和_。 不區分大小寫。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>屬性值。 不得包含 <span class="codeph"> &lt;cr&gt;</span> 或 <span class="codeph"> &lt;lf&gt;</span> 字元，除非在新行字元前有一個反斜線逸出。 </p></td> 
 </tr> 
</table>

Token之間的空白字元為選用。

具有未知屬性名稱的記錄會被 [!DNL Platform Server].

屬性名稱可包含ASCII字母、數字以及「 — 」、「_」和「。」的任意組合。

如果相同的屬性名稱在相同的屬性檔案中出現多次，則會以最後一個出現的屬性名稱為準。

使用#作為第一個字元，將任何記錄標籤為註解，解析器會忽略該註解。
