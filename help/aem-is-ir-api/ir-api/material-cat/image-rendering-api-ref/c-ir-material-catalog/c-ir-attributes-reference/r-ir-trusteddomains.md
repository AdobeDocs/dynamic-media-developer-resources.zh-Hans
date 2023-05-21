---
title: TrustedDomains
description: Flash應用程式網域。 AdobeFlash應用程式可能需要存取swf格式影像的屬性。 swf必須登入信任的應用程式網域名稱，才能明確授與存取權。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Flash應用程式網域。 AdobeFlash應用程式可能需要存取swf格式影像的屬性。 swf必須登入信任的應用程式網域名稱，才能明確授與存取權。

## 屬性 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

包含以逗號分隔的網路網域名稱清單的字串。 如果為空，則必須從與影像演算相同的網域提供應用程式，才能存取中影像的屬性 [!DNL swf] — 格式化回應。

## 默认 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

繼承自 `default::TrustedDomains` 如果不存在。

## 另请参阅 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ， `mask=`， [attribute：：RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
