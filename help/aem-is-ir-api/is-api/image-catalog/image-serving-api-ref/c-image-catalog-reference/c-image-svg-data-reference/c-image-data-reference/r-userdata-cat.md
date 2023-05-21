---
description: 使用者資料。 伺服器會傳回此欄位的內容給使用者端，以回應req=userdata。
solution: Experience Manager
title: 使用者資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# 使用者資料{#userdata}

使用者資料。 伺服器會傳回此欄位的內容給使用者端，以回應req=userdata。

## 屬性 {#section-06f2002b77d54a64be07f12fff54ad13}

文字字串值。 建議使用 [屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 格式化。 如果未使用屬性資料格式，文字字串不得包含&#39;=&#39;字元。

縮放、迴轉和小冊子檢視器使用者端會假設此欄位使用屬性資料格式。 這些使用者端使用此欄位進行檢視器設定和自訂。 如需詳細資訊，請參閱檢視器檔案。

此欄位參與文字字串本地化。 請參閱 [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP通訊協定參考* 以取得詳細資訊。

## 默认 {#section-7ee879762130467199745f2abc662f1e}

无。

## 另请参阅 {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
