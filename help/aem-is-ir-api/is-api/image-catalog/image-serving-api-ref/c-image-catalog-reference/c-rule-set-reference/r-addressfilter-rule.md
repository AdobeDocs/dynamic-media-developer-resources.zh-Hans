---
description: 位址篩選元素。 選填於 <rule> 和 <pathrule> 元素。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# 地址篩選器{#addressfilter}

位址篩選元素。 選填於 `<rule>` 和 `<pathrule>` 元素。

覆寫 `attribute::ClientAddressFilter` 套用規則時。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

无。

## 数据 {#section-c762bdfe425140d689ea5abf25e9a48a}

IP位址的逗號分隔清單。 每個個別位址都可包含選用的網路遮罩字尾，以指定IP位址範圍。 有关详细信息，请参阅`attribute::ClientAddressFilter`。

## 说明 {#section-d561b2485e004ef8a2085997d0f4bca6}

您可以透過在中指定一個或多個特定使用者端IP位址，來限制對此影像目錄的存取 `<addressfilter>` 元素。 如果使用者端IP位址不相符，則會傳回「請求被拒絕」錯誤給使用者端。

如果符合下列條件，則不會限制存取 `<addressfilter>` 為空白或未指定。

如果 `<expression>` 在 `<rule>` 元素不存在或空白， `<addressfilter>` 會套用至所有要求。

## 另请参阅 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute：：ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
