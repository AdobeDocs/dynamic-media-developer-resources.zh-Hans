---
title: 物件
description: 依名稱選取物件。 依名稱選取指定的暈映群組，並開始新的MSS。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# 物件{#obj}

依名稱選取物件。 依名稱選取指定的暈映群組，並開始新的MSS。

` obj= *`名称`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </p> </td> 
  <td class="stentry"> <p>群組名稱或路徑/名稱。 </p> </td> 
 </tr> 
</table>

子群組或個別物件可使用完全合格的群組路徑來選取(亦即，指定目標群組或物件的名稱，其前面有以/ （正斜線）分隔的所有父群組。

如果找不到具有指定名稱的群組/物件，則指定的動作會位於 `attribute::OnObjFail` 已採用。

## 屬性 {#section-9463b36e8ff74c81a70c7c2b58927430}

選取範圍指令；MSS分隔符號。 物件選取項會持續存在，直到選取其他物件為止，或是使用 `obj=` 或 `sel=`.

群組/物件路徑和名稱不區分大小寫。

## 默认 {#section-0c322850512c4896bb551856a549440e}

開啟新暈映時，會自動選取暈映中包含可轉譯物件的第一個群組。

## 另请参阅 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)， [attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
