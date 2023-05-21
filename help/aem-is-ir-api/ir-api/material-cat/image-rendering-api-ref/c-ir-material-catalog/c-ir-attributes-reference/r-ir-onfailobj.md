---
title: OnFailObj
description: 物件選取範圍錯誤處理。 指定當obj=命令因指定的路徑在暈映物件階層中不相符而失敗時要採取的動作。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# OnFailObj{#onfailobj}

物件選取範圍錯誤處理。 指定當obj=命令因指定的路徑在暈映物件階層中不相符而失敗時要採取的動作。

## 屬性 {#section-2c779d9c133a443d9f0aed9fde7b703c}

列舉。

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自 <span class="codeph"> default：：OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>保留先前的選取範圍。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>取消選取；會忽略任何套用材料或顯示/隱藏物件的嘗試。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>傳回錯誤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>選取預設群組（暈映階層中第一個包含可轉譯物件的群組）。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-a5a95a2b4a204a4eae350e5b544d1513}

繼承自 `default::OnFailObj` 若未定義。

## 另请参阅 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ， [attribute：：OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
