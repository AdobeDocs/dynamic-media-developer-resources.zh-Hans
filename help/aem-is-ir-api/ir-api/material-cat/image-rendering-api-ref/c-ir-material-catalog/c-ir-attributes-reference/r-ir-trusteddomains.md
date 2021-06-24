---
description: Flash应用程序Web域。 AdobeFlash应用程序可能需要访问以swf格式传送的图像的属性。swf必须通过注册它信任的应用程序域名来明确授予访问权限。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# TrustedDomains *{#trusteddomains}

Flash应用程序Web域。 AdobeFlash应用程序可能需要访问以swf格式传送的图像的属性。swf必须通过注册它信任的应用程序域名来明确授予访问权限。

## 属性 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

包含以逗号分隔的Web域名列表的字符串。 如果为空，则必须从与“图像渲染”相同的域为应用程序提供服务，才能访问[!DNL swf]格式响应中图像的属性。

## 默认 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

从`default::TrustedDomains`继承（如果不存在）。

## 另请参阅 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`，属 [性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
