---
description: 屬性資料包含代表一或多個屬性的文字字串。
solution: Experience Manager
title: 屬性資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# 屬性資料{#property-data}

屬性資料包含代表一或多個屬性的文字字串。

屬性包含屬性名稱和屬性值，以=分隔。

多個屬性以行分隔符號分隔，行分隔符號可能是 `??` 或 `<CR><LF>`. 如果整個屬性資料字串未括在引號中，則伺服器會取代每個出現的 `??` 替換為 `<CR><LF>` 將資料傳輸至使用者端之前。 屬性名稱可由字母、數字、&#39;.&#39;、&#39;-&#39;和&#39;_&#39;組成。 屬性名稱不區分大小寫。

屬性值不得包含行分隔符號。

另請參閱 [文字字串](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) 適用於屬性資料的其他規則。
