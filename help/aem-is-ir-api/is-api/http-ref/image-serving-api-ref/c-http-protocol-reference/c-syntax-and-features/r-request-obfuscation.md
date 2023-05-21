---
description: 套用標準base64編碼可能會遮蔽請求字串整個修飾元部分的內容，包括選用的鎖定尾碼。
solution: Experience Manager
title: 要求模糊化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 要求模糊化{#request-obfuscation}

套用標準base64編碼可能會遮蔽請求字串整個修飾元部分的內容，包括選用的鎖定尾碼。

如果符合下列條件，伺服器會嘗試解碼 `attribute::RequestObfuscation` 已設定。 如果解碼失敗，則會拒絕要求。 如果同時套用要求鎖定和要求模糊化，則必須在base64編碼之前產生並附加鎖定尾碼。

>[!IMPORTANT]
>
>如果您啟用此功能，請注意，其使用方式有一些限制，其中包括：<br>-Dynamic Media使用者介面可能不會顯示正確的詳細資料 **[!UICONTROL 上次發佈日期]** 欄位。 不過，此影響不會影響發佈。<br> — 目前，HLS視訊串流不適用於 **[!UICONTROL 要求模糊化]** 和 **[!UICONTROL 要求鎖定]** 已啟用。<br> — 目前，有些Dynamic Media檢視器在 **[!UICONTROL 要求模糊化]** 和 **[!UICONTROL 要求鎖定]** 已啟用。

## 示例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

編碼為：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

在要求模糊化之前，值字串中任何出現的&#39;=&#39;、&#39;&amp;&#39;和&#39;%&#39;都必須使用&#39;%xx&#39;編碼逸出。 您不一定要使用http編碼 *修飾元* 在模糊化之前或之後（即使套用要求鎖定）的部分要求，因為base64編碼對http傳輸是安全的。

## 另请参阅 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP編碼](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)， [要求鎖定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)， [屬性：：RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
