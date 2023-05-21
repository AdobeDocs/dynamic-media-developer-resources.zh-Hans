---
title: 輔助技術支援
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性預設為檢視器的名稱。 您可以使用以下專案控制標籤 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文字集 `aria-label` 屬性。 的值 `aria-label` 屬性會從按鈕本地化符號的值填入。 當按鈕停用時， `aria-disabled` 屬性會適當地設定。

滑桿元件具有此角色 `slider` 具有屬性 `aria-valuenow`， `aria-valuemin`、和 `aria-valuemax` 以說明目前的滑桿位置。

縮圖具有角色 `dialog` 替換為 `aria-label` 由控制的屬性 `ThumbnailGridView.LABEL` 本地化符號。 個別縮圖具有角色 `button`. 如果選取縮圖，則會取得 `aria-selected` 屬性設定為 `true`.

顯示色票的元件具有此角色 `listbox` 替換為 `aria-label` 屬性設為 `LABEL` 該元件的本地化符號。 個別色票有此角色 `option` 替換為 `aria-setsize` 和 `aria-posinset` 屬性來說明色票在色票集中的位置。 如果選取色票，則會取得 `aria-selected` 屬性設定為 `true`.

下拉式清單由具有其他功能的按鈕啟動 `aria-haspopup` 屬性設定為 `true` 和 `aria-controls` 屬性會參照實際的下拉式面板元素。 下拉式面板本身具有角色 `menu` 具有角色的子元素 `menuitem`. 每個功能表專案都有 `aria-label` 屬性已指定。

模型對話方塊具有角色 `dialog`. 對話方塊的標頭元素由 `aria-labelledby` 屬性。
