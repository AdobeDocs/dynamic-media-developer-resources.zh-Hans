---
description: Flash应用程序Web域。 Adobe Flash应用程序可能需要访问通过fmt=swf或fmt=swf3提供的图像的属性。
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Flash应用程序Web域。 Adobe Flash应用程序可能需要访问通过fmt=swf或fmt=swf3提供的图像的属性。

swf必须通过注册它信任的应用程序域的名称来明确授予访问权限。

## 属性 {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

包含以逗号分隔的Web域名列表的字符串。 如果为空，则必须从与图像渲染相同的域提供应用程序，才能访问swf格式响应中图像的属性。

## 默认 {#section-5c52ed3c7310488380f5a6f9540bf981}

从`default::TrustedDomains`继承（如果不存在）。

## 另请参阅 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
