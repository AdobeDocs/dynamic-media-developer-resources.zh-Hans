---
description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
solution: Experience Manager
title: 地址过滤器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 7%

---

# 地址过滤器{#addressfilter}

地址筛选器元素。 `<rule>`和`<pathrule>`元素中的可选。

应用规则时覆盖`attribute::ClientAddressFilter`。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

无。

## 数据 {#section-c762bdfe425140d689ea5abf25e9a48a}

IP地址的逗号分隔列表。 每个单独的地址可以包括一个可选的网络掩码后缀，以允许指定IP地址范围。 有关详细信息，请参阅`attribute::ClientAddressFilter`。

## 说明 {#section-d561b2485e004ef8a2085997d0f4bca6}

通过在`<addressfilter>`元素中指定一个或多个特定客户端IP地址，可以限制对此图像目录的访问。 如果客户端IP地址不匹配，则向客户端返回“请求被拒绝”错误。

如果`<addressfilter>`为空或未指定，则访问不受限制。

如果`<rule>`元素中的`<expression>`不存在或为空，则会将`<addressfilter>`应用于所有请求。

## 另请参阅 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute：：ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
