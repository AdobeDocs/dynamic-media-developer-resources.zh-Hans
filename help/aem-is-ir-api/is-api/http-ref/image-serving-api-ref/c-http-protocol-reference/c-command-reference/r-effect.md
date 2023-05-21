---
title: 效果
description: 選取效果圖層。 選取效果圖層，並在與目前圖層相關聯的請求字串中開始新的圖層區段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 3%

---

# 效果{#effect}

選取效果圖層。 選取效果圖層，並在與目前圖層相關聯的請求字串中開始新的圖層區段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果圖層編號（int不等於0）。 </p></td> 
 </tr> 
</table>

新區段內的所有指令都會套用至指定的效果圖層。 效果圖層區段由下一個終止 `layer=` 或 `effect=` 命令或要求結束前送出。

*`n`* 外部圖層效果（即父圖層後的效果）必須小於0，內部圖層效果（即父圖層內的效果）必須大於0。 效果圖層編號不一定要連續。

如果同一個父圖層有多個效果圖層，效果圖層編號會指定z順序。 編號較高的圖層會放置在編號較低的圖層的頂端。

效果圖層可以附加至 `layer=comp`.

## 屬性 {#section-e11f795deff345779ce280a82cf221ca}

效果圖層指令。 *`n`* 不得為0。

## 默认 {#section-84bbe1cfe7a94040827c994323ac59d4}

无。

## 示例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另请参阅 {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
