---
description: Flash应用程序Web域。 AdobeFlash应用程序可能需要访问使用fmt=swf或fmt=swf3传送的图像的属性。
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

Flash应用程序Web域。 AdobeFlash应用程序可能需要访问使用fmt=swf或fmt=swf3传送的图像的属性。

swf必须通过注册它信任的应用程序域的名称来明确授予访问权限。

## 属性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗号分隔的Web域名列表的字符串。 如果为空，则必须从与“图像渲染”相同的域提供应用程序，才能访问swf格式响应中图像的属性。

## 默认 {#section-5c52ed3c7310488380f5a6f9540bf981}

从`default::TrustedDomains`继承（如果不存在）。

## 另请参阅 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
