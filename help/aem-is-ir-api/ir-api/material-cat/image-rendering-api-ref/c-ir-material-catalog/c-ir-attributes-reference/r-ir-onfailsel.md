---
title: OnFailSel
description: 挑選選取範圍錯誤處理。 指定當sel=命令因指定的畫素位置不在可選取物件的遮色片區域內而失敗時，所要採取的動作。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# OnFailSel{#onfailsel}

挑選選取範圍錯誤處理。 指定在下列情況下要採取的動作： `sel=` 命令失敗，因為指定的畫素位置不在可選取物件的遮色片區域內。

## 屬性 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

列舉。

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>繼承自 <span class="codeph"> default：：OnFailSel </span>. </p> </td> 
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

## 默认 {#section-c25f458f9f8f4236963a95779529e664}

繼承自 `default::OnFailSel` 若未定義。

## 另请参阅 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ， [attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
