---
description: Flash应用程序Web域。 AdobeFlash应用程序可能需要访问使用fmt=swf或fmt=swf3传送的图像的属性。
seo-description: Flash应用程序Web域。 AdobeFlash应用程序可能需要访问使用fmt=swf或fmt=swf3传送的图像的属性。
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# TrustedDomains{#trusteddomains}

Flash应用程序Web域。 AdobeFlash应用程序可能需要访问使用fmt=swf或fmt=swf3传送的图像的属性。

swf必须通过注册其信任的应用程序域的名称来显式授予访问权限。

## 属性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗号分隔的Web域名列表的字符串。 如果为空，则必须从与图像渲染相同的域中提供应用程序，才能访问swf格式响应中图像的属性。

## 默认 {#section-5c52ed3c7310488380f5a6f9540bf981}

从`default::TrustedDomains`继承（如果不存在）。

## 另请参阅 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
