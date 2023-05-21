---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性預設為檢視器的名稱。 您可以使用以下專案控制標籤 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文字集 `aria-label` 屬性。 的值 `aria-label` 屬性會從按鈕本地化符號的值填入。 當按鈕停用時， `aria-disabled` 屬性會適當地設定。

滑桿元件具有此角色 `slider` 具有屬性 `aria-valuenow`， `aria-valuemin`、和 `aria-valuemax` 以說明目前的滑桿位置。

下拉式清單由具有其他功能的按鈕啟動 `aria-haspopup` 屬性設定為 `true` 和 `aria-controls` 屬性會參照實際的下拉式面板元素。 下拉式面板本身具有角色 `menu` 具有角色的子元素 `menuitem`. 每個功能表專案都有 `aria-label` 屬性已指定。

模型對話方塊具有角色 `dialog`. 對話方塊的標頭元素由 `aria-labelledby` 屬性。
