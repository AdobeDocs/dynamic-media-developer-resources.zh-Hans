---
title: RootId
description: 目录标识符。 HTTP路径元素，用于在HTTP请求的晕影、材质或ICC配置文件对象说明符中标识此目录。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cc34087a-8a19-4ead-b510-f2466efc44a9
TQID: 'https://experienceleague.adobe.com/Aglu-ZeC1g0LLlAwLDK5RZcgqBRyEE2NbmPodlRiJZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 4%

---

# RootId{#rootid}

目录标识符。 HTTP路径元素，用于在HTTP请求的晕影、材质或ICC配置文件对象说明符中标识此目录。

## 属性 {#section-c33266223d5b47029df756caa4e0df0c}

文本字符串值。 可以包含http路径中有效的任何字符。

## 默认 {#section-e0ed902557684345850b86672b5dbe5b}

无。 每个目录必须具有唯一的`catalog::RootId`值。 default.ini通常具有空的`catalog::RootId`。

## 另请参阅 {#section-4670832574f54f9080bb485b047efd5b}

[目录：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)，[晕影：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd)，[profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e)，[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)

