---
description: 為了減少篡改請求的機會，提供簡單的鎖定功能。
solution: Experience Manager
title: 要求鎖定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 要求鎖定{#request-locking}

為了減少篡改請求的機會，提供簡單的鎖定功能。

如果已設定attribute：：RequestLock，則必須將鎖定值附加至要求，格式為 `&xxxx`，其中xxxx是四位數的十六進位值。 此十六進位值是使用套用至 *修飾元* 請求部分（在「？」之後） 會將URL路徑與 *修飾元*)。 這必須在請求完全經過http編碼之後，但在請求被（可選）模糊化之前完成。 將請求去模糊化後，伺服器將對修飾元字串使用相同的雜湊演演算法（排除包含鎖定值的後5個字元）。 如果產生的鍵與鎖定不符，則會拒絕要求。

>[!IMPORTANT]
>
>如果您啟用此功能，請注意，其使用方式有一些限制，其中包括：<br>-Dynamic Media使用者介面可能不會顯示正確的詳細資料 **[!UICONTROL 上次發佈日期]** 欄位。 不過，此影響不會影響發佈。<br> — 目前，HLS視訊串流不適用於 **[!UICONTROL 要求模糊化]** 和 **[!UICONTROL 要求鎖定]** 已啟用。<br> — 目前，有些Dynamic Media檢視器在 **[!UICONTROL 要求模糊化]** 和 **[!UICONTROL 要求鎖定]** 已啟用。

產生請求鎖定值的C++範常式式碼：

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## 另请参阅 {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)， [要求模糊化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)， [attribute：：RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
