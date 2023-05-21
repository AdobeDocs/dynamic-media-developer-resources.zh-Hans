---
title: 错误
description: 如果要求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態以及錯誤訊息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# 错误{#errors}

如果要求無法成功完成，伺服器會傳回錯誤影像或200以外的HTTP回應狀態以及錯誤訊息。

回應狀態值取決於錯誤的型別；對於最常見的錯誤，值為「403」。 非影像要求型別的錯誤回應符合指定的格式 `req=`. （目前可能無法一致地實作。）

錯誤訊息中包含的詳細資訊量可通過以下方式設定： `attribute::ErrorDetail`.

**錯誤影像**

「影像伺服」可設定為傳回演算至影像的錯誤訊息。 另請參閱 `attribute::ErrorImage` 在影像目錄參考中取得詳細資訊。 如果成功產生錯誤影像，HTTP回應狀態為200。 如果在處理錯誤影像時發生錯誤，則會將標準HTTP錯誤回應和文字訊息傳回使用者端。

**另请参阅**

[attribute：：ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ， [attribute：：ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
