---
description: Flash應用程式網域。 AdobeFlash應用程式可能需要存取以fmt=swf或fmt=swf3傳遞的影像屬性。
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Flash應用程式網域。 AdobeFlash應用程式可能需要存取以fmt=swf或fmt=swf3傳遞的影像屬性。

swf必須登入信任的應用程式網域名稱，才能明確授與存取權。

## 屬性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗號分隔的網路網域名稱清單的字串。 如果為空，則必須從與影像演算相同的網域提供應用程式，才能存取SWF格式回應中影像的屬性。

## 默认 {#section-5c52ed3c7310488380f5a6f9540bf981}

繼承自 `default::TrustedDomains` 如果不存在。

## 另请参阅 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
