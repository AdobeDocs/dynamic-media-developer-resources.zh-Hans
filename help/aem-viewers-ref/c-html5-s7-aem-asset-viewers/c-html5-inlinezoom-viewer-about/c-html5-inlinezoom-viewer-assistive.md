---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性預設為檢視器的名稱。 您可以使用以下專案控制標籤 `Container.LABEL` 本地化符號。

主要檢視具有角色 `application`. 主要檢視的簡短說明請參閱 `aria-roledescription`，其值定義自 `ROLE_DESCRIPTION` 對應主要檢視元件的本地化符號。 為鍵盤使用者提供的導覽提示使用 `aria-describedby`，使用提示的文字來自 `USAGE_HINT` 本地化符號。 如果資產的UserData欄位中定義了標籤，則 `aria-label` 屬性是以此類標籤的值設定。

顯示色票的元件具有此角色 `listbox` 替換為 `aria-label` 屬性設為 `LABEL` 該元件的本地化符號。 個別色票有此角色 `option` 替換為 `aria-setsize` 和 `aria-posinset` 屬性來說明色票在色票集中的位置。 如果選取色票，則會取得 `aria-selected` 屬性設定為 `true`.
