---
description: 位址篩選元素。 選填於 <rule> 元素。 套用規則時覆寫屬性ClientAddressFilter。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 地址篩選器{#addressfilter}

位址篩選元素。 選填於 `<rule>` 元素。 套用規則時覆寫attribute：：ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP位址的逗號分隔清單。 每個個別位址都可包含選用的網路遮罩字尾，以指定IP位址範圍。 另請參閱 [attribute：：ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) 以取得詳細資訊。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

您可以透過在中指定一個或多個特定IP位址，來限制對此影像目錄的存取 `<addressfilter>` 元素。 如果使用者端IP位址不相符，則會傳回「請求被拒絕」錯誤給使用者端。

如果符合下列條件，則不會限制存取 `<addressfilter>` 為空白或未指定。

如果 `<expression>` 在 `<rule>` 元素不存在或空白， `<addressfilter>` 會套用至所有要求。

`localhost` 永遠是 `ClientAddressFilter` 定義，即使未明確指定。 請求來自 `localhost` 不會被拒絕，不論 `ClientAddressFilter` 規格。

## 另請參閱 {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute：：ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
