---
description: 所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。
solution: Experience Manager
title: 輔助技術支援
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 輔助技術支援{#assistive-technology-support}

所有檢視器元件都支援ARIA （可存取的豐富網際網路應用程式）角色和屬性，以改進與熒幕閱讀器等輔助技術的整合。

頂層檢視器元素具有角色 `region` 和 `aria-label` 屬性預設為檢視器的名稱。 您可以使用以下專案控制標籤 `Container.LABEL` 本地化符號。

按鈕具有角色 `button` 和描述性文字的設定 `aria-label` 屬性。 的值 `aria-label` 屬性會從按鈕本地化符號的值填入。 當按鈕停用時， `aria-disabled` 屬性會適當地設定。

主要檢視具有角色 `application`. 主要檢視的簡短說明請參閱 `aria-roledescription`，其值定義自 `ROLE_DESCRIPTION` 對應主要檢視元件的本地化符號。 為鍵盤使用者提供的導覽提示使用 `aria-describedby`，使用提示的文字來自 `USAGE_HINT` 本地化符號。 如果資產的UserData欄位中定義了標籤，則 `aria-label` 屬性是以此類標籤的值設定。

熱點、區域和影像地圖具有此角色 `button` 和描述性文字集 `aria-label` 屬性，具有連結區或影像地圖示籤的值。 當使用者聚焦於熱點或影像地圖時，會使用為鍵盤使用者提供導覽提示 `aria-describedby`，使用提示的文字來自 `USAGE_HINT` 本地化符號。

縮圖具有角色 `dialog` 替換為 `aria-label` 由控制的屬性 `ThumbnailGridView.LABEL` 本地化符號。 個別縮圖具有角色 `button`. 如果選取縮圖，則會取得 `aria-selected` 屬性設定為 `true`.

顯示色票的元件具有此角色 `listbox` 替換為 `aria-label` 屬性設為 `LABEL` 該元件的本地化符號。 個別色票有此角色 `option` 替換為 `aria-setsize` 和 `aria-posinset` 屬性來說明色票在色票集中的位置。 如果選取色票，則會取得 `aria-selected` 屬性設定為 `true`.

下拉式清單由具有其他功能的按鈕啟動 `aria-haspopup` 屬性設定為 `true` 和 `aria-controls` 屬性會參照實際的下拉式面板元素。 下拉式面板本身具有角色 `menu` 具有角色的子元素 `menuitem`. 每個功能表專案都有 `aria-label` 屬性已指定。

搜尋使用者介面會以角色分組在元素中 `search`. 搜尋輸入欄位具有角色 `searchbox` 和參考由控制的資訊性標籤 `SearchPanel.INFO_PROMPT` 本地化符號 `aria-describedby` 屬性。

模型對話方塊具有角色 `dialog`. 對話方塊的標頭元素由 `aria-labelledby` 屬性。
