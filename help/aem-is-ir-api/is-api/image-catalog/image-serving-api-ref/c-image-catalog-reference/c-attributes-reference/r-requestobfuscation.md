---
description: 请求模糊处理模式。 指定必须应用于有效请求的混淆类型。
solution: Experience Manager
title: 请求模糊处理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c330c8de-9539-442f-a52a-786f882873cf
TQID: 'https://experienceleague.adobe.com/IF7qVWoidj-WvoY-wR-D8uqkiTV3X44C7i4YzeyBbTI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 66
ht-degree: 1%

---

# 请求模糊处理{#requestobfuscation}

请求模糊处理模式。 指定必须应用于有效请求的混淆类型。

## 属性 {#section-0819432615324e259f24717e16835427}

枚举。 设置为0可禁用请求模糊处理，设置为1可选择base64编码。 目前不支持其他模糊处理方法。

## 默认 {#section-e7f49493d9a940acb4f7938df7cac44d}

如果未定义或为空，则从`default::RequestObfuscation`继承。
