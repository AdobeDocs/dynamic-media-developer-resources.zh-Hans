---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets,Accessibility
role: Developer,User
exl-id: f0cde820-237c-4594-8a16-d272af4c976b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性預設為檢視器的名稱。 您可以使用以下專案控制標籤 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文字集 `aria-label` 屬性。 的值 `aria-label` 屬性會從按鈕本地化符號的值填入。 當按鈕停用時， `aria-disabled` 屬性會適當地設定。

主要檢視具有角色 `application`. 主要檢視的簡短說明請參閱 `aria-roledescription`，其值定義自 `ROLE_DESCRIPTION` 對應主要檢視元件的本地化符號。 為鍵盤使用者提供的導覽提示使用 `aria-describedby`，使用提示的文字來自 `USAGE_HINT` 本地化符號。 如果資產的UserData欄位中定義了標籤，則 `aria-label` 屬性是以此類標籤的值設定。
