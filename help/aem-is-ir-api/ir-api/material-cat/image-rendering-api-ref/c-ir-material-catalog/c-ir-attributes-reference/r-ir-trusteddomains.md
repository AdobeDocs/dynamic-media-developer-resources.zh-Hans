---
description: Flash应用程序Web域。 Adobe Flash应用程序可能需要访问以swf格式传送的图像的属性。swf必须通过注册其信任的应用程序域的名称来显式授予访问权。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# TrustedDomains *{#trusteddomains}

Flash应用程序Web域。 Adobe Flash应用程序可能需要访问以swf格式传送的图像的属性。swf必须通过注册其信任的应用程序域的名称来显式授予访问权。

## 属性 {#section-5d6ecfa431a04abd8628a28e0ab3be83}

包含以逗号分隔的Web域名列表的字符串。 如果为空，则必须从与图像渲染相同的域中提供应用程序，才能访问[!DNL swf]格式化响应中图像的属性。

## 默认 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

从`default::TrustedDomains`继承（如果不存在）。

## 另请参阅 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [属性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
